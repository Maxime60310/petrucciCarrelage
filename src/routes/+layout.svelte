<script lang="ts">
  import '$lib/scss/main.scss';
	import Nav from '$lib/components/Nav.svelte';  
	import favicon from '$lib/img/favicon.svg';
	import Header from '$lib/components/Header.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>
<Nav />
<Header />
{@render children()}
