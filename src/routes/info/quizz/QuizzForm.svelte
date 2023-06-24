<script>
    import { createEventDispatcher } from 'svelte';
    import { supabase } from '../../../supabaseClient';
    import { onMount } from 'svelte';
  
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
    function nextQuestion() {
      saveAnswer();
      currentQuestion += 1;
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
  
  <main>
    {#if currentQuestion < questions.length}

    <div class="w-1/3 px-4">
      <div class="bg-white rounded-lg shadow-md p-6 w-full h-auto">
      <h2 class="text-xl font-bold mb-2">{questions[currentQuestion].question}  </h2>
      <p class="text-gray-700 mb-4">Ecotaxe, gilets jaunes, marché carbone... Un point sur la fiscalité carbone! <br> Testez vos connaissances sur le sujet! </p>
      <a href="/info" class="text-lg bg-blue-500  hover:bg-blue-600 text-white font-bold py-2 px-4 rounded block text-center">S'informer</a>
      </div>
    </div>

      <div>
        <label>
          <input type="radio" bind:group={questions[currentQuestion].userAnswer} value="true" />
          VRAI
        </label>
        <label>
          <input type="radio" bind:group={questions[currentQuestion].userAnswer} value="false" />
          FAUX
        </label>
        <label>
          <input type="radio" bind:group={questions[currentQuestion].userAnswer} value="unknown" />
          JE NE SAIS PAS
        </label>
      </div>
      <button on:click={nextQuestion} disabled={questions[currentQuestion].userAnswer === null}>
        Suivant
      </button>
    {:else}
      <p>Toutes les questions ont été répondues.</p>
      <button on:click={submitAnswers} disabled={questions.some(question => question.userAnswer === null)}>
        Soumettre les réponses
      </button>
    {/if}
  </main>
  