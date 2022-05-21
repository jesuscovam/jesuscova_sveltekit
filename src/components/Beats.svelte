<script lang="ts">
	interface Song {
		title: string;
		src: string;
	}
	const songs: Song[] = [
		{
			title: 'foot fungus remake',
			src: '/songs/foot_fungus_remake.mp3'
		},
		{
			title: 'rocky raccoon',
			src: '/songs/rocky_raccoon.mp3'
		},
		{
			title: 'tranquilito',
			src: '/songs/tranquilito.mp3'
		}
	];
</script>

<section class="w-full">
	<h2 class="text-lg font-bold">BEATS</h2>
	<div class="mt-4">
		{#each songs as { title, src }}
			<div class="mt-2 flex flex-col space-y-2">
				<p class="font-medium text-sky-400">{title}</p>

				<audio controls {src} />
			</div>
		{/each}
	</div>
</section>
