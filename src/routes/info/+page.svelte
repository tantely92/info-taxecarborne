<script>
    import Info from "./Info.svelte";
	import Quizz from "./quizz/Quizz.svelte";

	import { beforeUpdate, onMount } from 'svelte';

	let state = {
		component:'quizz',
		result:'',
	};

	let displayComponent = null;
	onMount(() => {
		const infoState = localStorage.getItem('infoState');
		if (infoState){
			const{ component, result } = JSON.parse(infoState);
			state.component = component;
			state.result = result;
		}
		else{
			state.component = 'quizz';
		}
  	});

	

  // Fonction pour changer l'affichage des sous-composants
	function updateFromQuizzResult(event) {
		displayComponent = "infos";
		state.result = event.detail;
		state.component = "infos";
		localStorage.setItem('infoState', JSON.stringify(state));
	}
</script>


<svelte:head>
	<title>S'informer</title>
	<meta name="description" content="Information sur la taxe carbone" />
</svelte:head>
<div>
	{#if state.component === "quizz"}
		<Quizz on:quizzResult={updateFromQuizzResult}/>
	{/if}

	{#if state.component === "infos"}
		<Info/>
	{/if}
	
</div>