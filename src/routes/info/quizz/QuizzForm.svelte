<script>
    import { createEventDispatcher } from 'svelte';
    import { supabase } from '../../../supabaseClient';
    import { onMount } from 'svelte';
    import { fade } from 'svelte/transition';

    // Liste des questions et réponses
    let questions = [];
    
    onMount(async () => {
  
        const data = await fetchQuestions();
        questions = data;
      });
  
      // Fonction pour récupérer les questions depuis Supabase
      const fetchQuestions = async () => {
        const { data, error } = await supabase
          .from('questions')
          .select('id, text, answer');
  
        if (error) {
          console.error(error);
          return [];
        }
  
        const questionsList = data.map((question) => ({
          id: question.id,
          question: question.text,
          answer : question.answer.toString(),
          userAnswer: null // Remplacez cette valeur par la logique d'obtention de la réponse correspondante
        }));
  
        return questionsList;
      };
  
    let currentQuestion = 0; // Index de la question actuelle
    let score = 0;
    // Fonction pour passer à la question suivante
    function nextQuestion(answer) {
      questions[currentQuestion].userAnswer = answer
      saveAnswer();
      currentQuestion += 1;
      if ( currentQuestion >= questions.length ){
        submitAnswers();
      }
    }
  
    // Fonction pour sauvegarder la réponse
    function saveAnswer() {
      const isCorrect = questions[currentQuestion].userAnswer === questions[currentQuestion].answer;
      if ( isCorrect ){
        score = score + 1;
      }
    }
  
    // Fonction pour réinitialiser les réponses
    function resetAnswers() {
      questions.forEach(question => {
        question.answer = null;
      });
      currentQuestion = 0;
      score = 0;
    }
  
    function generateUserId() {
      const characters = 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789';
      const length = 10; // Longueur de l'identifiant utilisateur
      
      let userId = '';
      
      for (let i = 0; i < length; i++) {
        const randomIndex = Math.floor(Math.random() * characters.length);
        userId += characters[randomIndex];
      }
      
      return userId;
  }
  
    const dispatch = createEventDispatcher();
  
    // Fonction pour soumettre les réponses
    function submitAnswers() {
      const userId = generateUserId();
      const savedData = questions.map(question => ({ questionId : question.id, userId : userId, answer: question.userAnswer }));
      let resultat = null;
      // Insérer les données dans la base de données Supabase
      supabase
              .from('answers') 
              .insert(savedData)
              .then(response => {
              console.log('Données insérées avec succès:', response);
              // Effectuer d'autres actions après l'insertion des données
              },
              error => console.error('Erreur lors de l\'insertion des données:', error));
      if (score <= 5 ){
        resultat = 'infos taxecarbone tombe à pic pour vous informer';
      }
      else if ( score <= 8 ){
        resultat = 'vous avez des connaissances solides sur le sujet!';
      }
      else {
        resultat = 'il n\'y a plus de secret pour vous, nous avons hâte de connaître vos positions!'
      }
      dispatch('submit', resultat);
      resetAnswers();
    }
  </script>

<main class='flex items-center justify-center h-screen pt-10 pb-10 background10'>
  {#if currentQuestion < questions.length}
  <div class="flex flex-col justify-between bg-white rounded-lg shadow-md p-6 w-96 h-96">
      <div transition:fade>
          <h2 class="text-xl font-bold mb-2">{questions[currentQuestion].question}</h2>
      </div>
      <div class="relative inset-x-0 bottom-0 h-auto">
          <a href="#" on:click={() => { nextQuestion('true')} } class="text-lg bg-blue-100  hover:bg-green-600 text-gray-700 font-bold py-2 px-4 rounded block text-center">VRAI</a>
          <a href="#" on:click={() => { nextQuestion('false')} } class="text-lg bg-blue-100  hover:bg-red-600 text-gray-700 font-bold py-2 px-4 rounded block text-center">FAUX</a>
          <a href="#" on:click={() => { nextQuestion('unknown')} } class="text-lg bg-blue-100  hover:bg-blue-600 text-gray-300 font-bold py-2 px-4 rounded block text-center">JE NE SAIS PAS</a>
      </div>
  </div>
  {/if}
</main>


<style>
.background10 {
  background-image: linear-gradient(rgba(255, 255, 255, 0.7), rgba(255, 255, 255, 0.7)), url('Livrearbre.png');
  background-size: cover;
  background-position: center;
}

</style>