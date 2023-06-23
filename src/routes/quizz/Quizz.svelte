<script>
    import { createClient } from '@supabase/supabase-js';
    import { onMount } from 'svelte';

    const supabaseUrl = import.meta.env.VITE_SUPABASE_URL;
    const supabaseKey = import.meta.env.VITE_SUPABASE_KEY;
    const supabase = createClient(supabaseUrl, supabaseKey);
      // @ts-ignore
      
    
    

/**
   * @type {any[]}
   */
let questions = [];

    onMount(async () => {

      const response = await fetchQuestions();
      questions = response;
    });

    // Fonction pour récupérer les questions depuis Supabase
    const fetchQuestions = async () => {
      const { data, error } = await supabase
        .from('questions')
        .select('id, text');

      if (error) {
        console.error(error);
        return [];
      }

      const questionsList = data.map((question) => ({
        id: question.id,
        question: question.text,
        answer: '' // Remplacez cette valeur par la logique d'obtention de la réponse correspondante
      }));

      return questionsList;
    };

    let answers = {};
  
    /**
   * @param {Event & { currentTarget: EventTarget & HTMLInputElement; }} event
   * @param {string | number} questionId
   */
    function handleAnswer(event, questionId) {
      // @ts-ignore
      const value = event.target.value;
      // @ts-ignore
      answers[questionId] = value;
    }
  
    function handleSubmit() {
      // Traitement des réponses du formulaire
      // @ts-ignore
      questions = questions.map(question => ({ ...question, answer: answers[question.id] }));
      console.log(questions);
    }

    function handleSubmitDb() {
        // Traitement des réponses du formulaire
        let saved = [];
        saved = questions.map(question => ({ questionId : question.id, userId : 'Toto', answer: answers[question.id] }));
        console.log(saved);

        // Insérer les données dans la base de données Supabase
        supabase
            .from('answers') // Remplacez 'table_name' par le nom réel de votre table
            .insert(saved)
            .then(response => {
            console.log('Données insérées avec succès:', response);
            // Effectuer d'autres actions après l'insertion des données
            answers = {};
            },
            error => console.error('Erreur lors de l\'insertion des données:', error));
}

  </script>
  
  <main>
    <h1 class="text-4xl font-bold mb-4 ml-4">Liste de questions</h1>
  
    <form on:submit|preventDefault={handleSubmitDb} class="ml-4">
      {#each questions as question}
        <div class="mb-4">
          <p>{question.question}</p>
          <div class="flex items-center mt-2">
            <label class="inline-flex items-center">
              <input type="radio" class="form-radio" name={`question-${question.id}`} value="true" on:change={event => handleAnswer(event, question.id)} checked={answers[question.id] === 'true'} />
              <span class="ml-2">Vrai</span>
            </label>
            <label class="inline-flex items-center ml-4">
              <input type="radio" class="form-radio" name={`question-${question.id}`} value="false" on:change={event => handleAnswer(event, question.id)} checked={answers[question.id] === 'false'} />
              <span class="ml-2">Faux</span>
            </label>
          </div>
        </div>
      {/each}
  
      <button type="submit" class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded">Soumettre</button>
    </form>
  </main>
  
  

  
  