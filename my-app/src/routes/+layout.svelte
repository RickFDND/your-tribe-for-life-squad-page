<script>
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();

	import { onNavigate } from '$app/navigation';

	onNavigate((navigation) => {
	if (!document.startViewTransition) return;
	let viewTransitionType = 'page-change';
	if (navigation.type === 'goto') {
		return;
	}
	return new Promise((resolve) => {
		document.startViewTransition({
			update: async () => {
				resolve();
				await navigation.complete;
			},
			types: [viewTransitionType]
		});
	});
});
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children?.()}


