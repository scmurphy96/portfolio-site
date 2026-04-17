<script lang="ts">
	import '../app.css';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" type="image/jpeg" href="/headshot.jpg" />
	<title>Sean Murphy</title>
	<meta name="description" content="Sean Murphy - Personal Portfolio" />
</svelte:head>

{@render children()}
