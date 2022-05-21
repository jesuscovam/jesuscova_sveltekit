<script>
	import '../styles.css';
</script>

<svelte:head>
	<link
		rel="icon"
		href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>🐸</text></svg>"
	/>
	<title>jesus</title>
</svelte:head>

<div class="py-2 bg-gradient-to-r from-blue-400 via-indigo-500 to-cyan-400" />
<main class="bg-black text-sky-blue">
	<slot />
</main>
<footer class="w-full bg-black pt-10 text-center pb-5">
	<a
		href="https://github.com/jesuscovam/jesuscova-svelte"
		target="_blank"
		class="text-sky-400 underline"
	>
		code from this website
	</a>
</footer>
