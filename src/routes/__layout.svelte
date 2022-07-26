<script>
	import Header from '$lib/header.svelte';
	import '../tailwind.css';

	const date = new Date();
	const year = date.getFullYear();
</script>

<Header />

<main class="bg-blue-500">
	<slot />
</main>

<footer>&copy;Copyright {year}</footer>

<style lang="scss">
</style>
