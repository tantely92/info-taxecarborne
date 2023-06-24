<script>
    import QuizzForm from './QuizzForm.svelte';
    import { createEventDispatcher } from 'svelte';

    const dispatch = createEventDispatcher();

    let activeQuizz = false;
    let resultat = null;
    let showResult = false;

    function displayQuizz(){
        console.log('display quizz');
        activeQuizz = true;
    }

    function showResultQuizz(event){
        activeQuizz= false;
        resultat = event.detail;
        if ( resultat === null ){
            resultat = '';
        }

        dispatch('quizzResult',resultat);
    }
</script>

<div class="absolute w-full top-40 flex flex-col items-center  bg-gradient-to-r from-blue-200">
    {#if !activeQuizz}
    <div>
      <button class="pulse bg-blue-500 hover:bg-red-600 transform transition-transform duration-200 text-white font-bold py-2 px-4 rounded mb-10 mt-10" on:click={() => displayQuizz()}>
        Testez d'abord vos connaissances! 
      </button>
    </div>
    {/if}
    <div>
        {#if activeQuizz === true}
        <QuizzForm on:submit={showResultQuizz} />
        {/if}
        {#if showResult === true}
        <div>{resultat}</div>
        {/if}
        <img src="Livrearbre.png" alt="Image" class="w-full blur-sm">
    </div>
</div>

<style>
@keyframes pulse {
  0% { transform: scale(1); background-color: #3B82F6;}
  50% { transform: scale(1.1); background-color: #EF4444; }
  100% { transform: scale(1); background-color: #3B82F6;}
}

.pulse {
  animation: pulse 1s infinite;
}
</style>
