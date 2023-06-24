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
    <div>
      <button class="bg-blue-500 hover:bg-blue-600 transform hover:scale-105 transition-transform duration-200 text-white font-bold py-2 px-4 rounded mb-4" on:click={() => displayQuizz()}>
        Testez d'abord vos connaissances! 
      </button>
      
    </div>
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

<div >
    
    
</div>

<style></style>
    