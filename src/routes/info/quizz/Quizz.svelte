<script>
    import QuizzForm from './QuizzForm.svelte';
    let activeQuizz = false;
    let resultat = null;
    let showResult = false;

    function displayQuizz(){
        if ( resultat != null ){
            alert('Vous avez déjà répondu au quizz avec le résultat :', resultat);
        }
        else{
            activeQuizz = true
        }
        
    }

    function showResultQuizz(event){
        activeQuizz= false;
        resultat = event.detail;
        if ( resultat != null ){
            showResult = true;
        }else{
            alert('erreur lors de la récupération du résultat')
        }
        console.log(resultat);
    }
</script>

<div class="flex justify-center mt-4">
    <div>
      <button class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4" on:click={() => displayQuizz()}>
        Testez d'abord vos connaissances! 
      </button>
    </div>
</div>

<div >
    
    {#if activeQuizz === true}
      <QuizzForm on:submit={showResultQuizz} /> <!-- Remplacez 'TestComponent' par le nom de votre composant Svelte -->
    {/if}
    {#if showResult === true}
      <div>{resultat}</div>
    {/if}
</div>

<style></style>
    