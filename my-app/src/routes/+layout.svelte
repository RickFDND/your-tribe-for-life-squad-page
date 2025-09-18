<script>
	import favicon from '$lib/assets/favicon.svg'; 

	let { children } = $props();

	import { onNavigate } from '$app/navigation';

	onNavigate((navigation) => { // View Transition API
	if (!document.startViewTransition) return; // Controleer of de View Transition API wordt ondersteund
	let viewTransitionType = 'page-change'; 
	if (navigation.type === 'goto') { // Alleen bij 'goto' navigaties
		return;
	}
	return new Promise((resolve) => {
		document.startViewTransition({ // Start de view transition
			update: async () => {
				resolve();
				await navigation.complete; // Wacht tot de navigatie is voltooid
			},
			types: [viewTransitionType] // Specificeer het type overgang
		});
	});
});
</script>

<svelte:head>
	<link rel="icon" href={favicon} /> <!-- Voeg de favicon toe aan de head van het document -->
</svelte:head>

{@render children?.()} <!-- Render de kinderen van de layout, wat de inhoud van de pagina zal zijn -->


