<script prerender: false>
    import Info from "./Info.svelte";
	import Quizz from "./quizz/Quizz.svelte";

	import { setContext, getContext, onMount } from 'svelte';
	import { writable } from 'svelte/store';

	const state = writable({
		component:'quizz',
		result:'',
	});

	let displayComponent = null;
	onMount(() => {
		const infoState = localStorage.getItem('infoState');
		if (infoState){
			const{ component, result } = JSON.parse(infoState);
			displayComponent = component;
		}
		else{
			displayComponent = 'quizz';
		}

		state.subscribe(newState => {
			// Sauvegardez l'état dans le stockage local à chaque modification
			console.log("new state");
			localStorage.setItem('infoState', JSON.stringify(newState));
		});
		console.log('onMount ',infoState);
  });

  // Fonction pour changer l'affichage des sous-composants
	function updateFromQuizzResult(event) {
		displayComponent = "infos";
		state.result = event.detail;
		state.component = "infos";
		localStorage.setItem('infoState', JSON.stringify(state));
		alert(state.result);
	}
</script>


<svelte:head>
	<title>S'informer</title>
	<meta name="description" content="Information sur la taxe carbone" />
</svelte:head>
<div>
	{#if displayComponent === "quizz"}
		<Quizz on:quizzResult={updateFromQuizzResult}/>
	{/if}

	{#if displayComponent === "infos"}
		<Info/>
	{/if}
</div>
<Info/>