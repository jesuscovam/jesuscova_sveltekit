<script lang="ts">
	const ETH_WALLET = '0x928716fCC08817db3f608FE94F78705ceA370a44' as const;
	const ETH_WALLET_SHORT = `${ETH_WALLET.slice(0, 5)}...${ETH_WALLET.slice(ETH_WALLET.length - 4)}`;

	const links = [
		{
			url: 'https://www.twitter.com/jesusacova',
			label: 'twitter'
		},
		{
			url: 'https://www.github.com/jesuscovam',
			label: 'github'
		},
		{
			url: '',
			label: ETH_WALLET_SHORT
		}
	];

	const copyAddress = () => {
		navigator.clipboard.writeText(ETH_WALLET);
		alert('copiado');
	};
</script>

<section class="flex flex-col mx-auto space-y-2 ">
	<img src="/jesus.webp" alt="mi persona" class="w-60 h-60 rounded-2xl self-center mb-5" />
	<div class="border-2 border-white w-32 px-2 rounded-lg">
		<h1 class="text-white text-center">JESUS COVA</h1>
	</div>
	{#each links as link}
		{#if link.url === ''}
			<button on:click={copyAddress} class="text-sky-400 underline self-start">{link.label}</button>
		{:else}
			<a href={link.url} class="text-sky-400 underline">{link?.label}</a>
		{/if}
	{/each}
</section>
