<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';
	import '../app.css';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<title>Sean Murphy</title>
	<meta name="description" content="Sean Murphy - Personal Portfolio" />
</svelte:head>

{@render children()}
