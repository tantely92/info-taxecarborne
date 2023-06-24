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

<div class="absolute w-full h-full top-0 left-0 flex flex-col items-center background10">
    {#if !activeQuizz}
    <div class="centered-content">
      <button class="pulse bg-blue-500 hover:bg-red-600 transform transition-transform duration-200 text-white text-2xl font-bold py-4 px-4 rounded" on:click={() => displayQuizz()}>
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


.background10 {
    background-image: linear-gradient(rgba(255, 255, 255, 0.7), rgba(255, 255, 255, 0.7)), url('Nouveautetaxe.png');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}

.centered-content {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100%;
}


</style>
