<script>
    import { createClient } from '@supabase/supabase-js';

    const supabaseUrl = 'https://your-supabase-url.supabase.co';
    const supabaseKey = 'your-supabase-api-key';
    const supabase = createClient(supabaseUrl, supabaseKey);

    let questions = [
      { id: 1, question: 'La Terre est plate', answer: null },
      { id: 2, question: 'Le soleil tourne autour de la Terre', answer: null },
      { id: 3, question: 'L\'eau bout à 100 degrés Celsius', answer: null }
    ];
  
    let answers = {};
  
    function handleAnswer(event, questionId) {
      const value = event.target.value;
      answers[questionId] = value;
    }
  
    function handleSubmit() {
      // Traitement des réponses du formulaire
      questions = questions.map(question => ({ ...question, answer: answers[question.id] }));
      console.log(questions);
    }
    function handleSubmitDb() {
        // Traitement des réponses du formulaire
        questions = questions.map(question => ({ ...question, answer: answers[question.id] }));
        console.log(questions);

        // Insérer les données dans la base de données Supabase
        supabase
            .from('table_name') // Remplacez 'table_name' par le nom réel de votre table
            .insert(questions)
            .then(response => {
            console.log('Données insérées avec succès:', response);
            // Effectuer d'autres actions après l'insertion des données
            })
            .catch((/** @type {any} */ error) => {
            console.error('Erreur lors de l\'insertion des données:', error);
            // Gérer les erreurs d'insertion des données
            });
}

  </script>
  
  <main>
    <h1 class="text-4xl font-bold mb-4 ml-4">Liste de questions</h1>
  
    <form on:submit|preventDefault={handleSubmit} class="ml-4">
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
  
  

  
  