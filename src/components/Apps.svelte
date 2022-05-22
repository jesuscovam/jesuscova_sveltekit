<script lang="ts">
	const num = 4555113009808710;

	interface App {
		url: string;
	}

	const apps: App[] = [
		{
			url: 'https://slissto.com'
		},
		{
			url: 'https://nfts.jesuscova.com'
		}
	];

	const displayUrl = (url: string) => url.slice(8);
</script>

<section class="flex flex-col space-y-2 text-white">
	<h2>APPS</h2>
	{#each apps as app}
		<a href={app.url} class="text-sky-500 underline">{displayUrl(app.url)}</a>
	{/each}
</section>
