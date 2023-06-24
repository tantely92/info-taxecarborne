<script>
  import { createEventDispatcher } from 'svelte';
  import { supabase } from '../../supabaseClient';
  import { onMount } from 'svelte';

  // Liste des questions et réponses
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
        answer: null // Remplacez cette valeur par la logique d'obtention de la réponse correspondante
      }));

      return questionsList;
    };

  let currentQuestion = 0; // Index de la question actuelle

  // Fonction pour passer à la question suivante
  function nextQuestion() {
    currentQuestion += 1;
  }

  // Fonction pour sauvegarder la réponse
  function saveAnswer(answer) {
    questions[currentQuestion].answer = answer;
    nextQuestion();
  }

  // Fonction pour réinitialiser les réponses
  function resetAnswers() {
    questions.forEach(question => {
      question.answer = null;
    });
    currentQuestion = 0;
  }

  const dispatch = createEventDispatcher();

  // Fonction pour soumettre les réponses
  function submitAnswers() {
    const answers = questions.map(question => question.answer);
    dispatch('submit', answers);
    resetAnswers();
  }
</script>

<main>
  {#if currentQuestion < questions.length}
    <h2>{questions[currentQuestion].question}</h2>
    <div>
      <label>
        <input type="radio" bind:group={questions[currentQuestion].answer} value="true" />
        VRAI
      </label>
      <label>
        <input type="radio" bind:group={questions[currentQuestion].answer} value="false" />
        FAUX
      </label>
      <label>
        <input type="radio" bind:group={questions[currentQuestion].answer} value="unknown" />
        JE NE SAIS PAS
      </label>
    </div>
    <button on:click={nextQuestion} disabled={questions[currentQuestion].answer === null}>
      Suivant
    </button>
  {:else}
    <p>Toutes les questions ont été répondues.</p>
    <button on:click={submitAnswers} disabled={questions.some(question => question.answer === null)}>
      Soumettre les réponses
    </button>
  {/if}
</main>
