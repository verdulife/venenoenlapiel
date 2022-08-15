<script>
	import { events } from '$lib/data';
	import Event from '$lib/components/Event.svelte';
	import { onMount } from 'svelte';

	let slider;

	function prev() {
		slider.scrollBy({
			left: -1
		});
	}

	function next() {
		slider.scrollBy({
			left: 1
		});
	}

	onMount(() => {
		slider = document.querySelector('.slider');
	});
</script>

<section id="events" class="viewport col fcenter">
	<h2>Próximos conciertos</h2>

	<ul class="slider snap">
		{#each events as event}
			<li class="slide">
				<Event data={event} />
			</li>
		{/each}
	</ul>

	<div class="controls row">
		<button class="prev row fcenter" on:click={prev}>
			<img src="/prev.svg" alt="Anterior" />
		</button>

		<button class="next row fcenter" on:click={next}>
			<img src="/next.svg" alt="Siguiente" />
		</button>
	</div>
</section>

<style lang="scss">
	section {
		background: #000;
	}

	h2 {
		font-size: 40px;
		color: #fff;
		font-family: var(--font-title);
	}

	.slider {
		max-width: 1100px;
		margin-top: 60px;
	}

	.slide {
		margin-left: 20px;
	}

	.controls {
		gap: 20px;
		font-family: var(--font-text);
		margin-top: 30px;

		button {
			width: 60px;
			height: 60px;
			background: rgba(#fff, 0.1);
			color: #fff;
		}
	}
</style>
