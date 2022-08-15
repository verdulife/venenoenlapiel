<script>
	import { volumeState } from '$lib/stores';
	import { onMount } from 'svelte';

	let video;

	$: if (video) {
		video.muted = !$volumeState;
	}

	onMount(() => {
		video = document.querySelector('video');
	});
</script>

<div class="video-wrapper fill">
	<video class="fill cover" autoplay muted loop playsinline>
		<source src="/bg.mp4" type="video/mp4" />
	</video>
</div>

<style lang="scss">
	.video-wrapper {
		position: absolute;
		top: 0;
		left: 0;
		z-index: 0;

		&:after {
			content: '';
			position: absolute;
			inset: 0;
			background: rgba(0, 0, 0, 0.5);
			pointer-events: none;
		}
	}
</style>
