<script lang="ts">
	import Nav from '$lib/components/Nav.svelte';  
	import favicon from '$lib/img/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>
<Nav />
{@render children()}
