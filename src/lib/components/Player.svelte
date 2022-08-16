<script>
	import { volumeState } from '$lib/stores';

	function togVolume() {
		$volumeState = !$volumeState;
	}
</script>

<div class="volume btn row fcenter" on:click={togVolume}>
	<img src="/{$volumeState ? 'volume' : 'mute'}.svg" alt="Sonido" />
</div>

<style lang="scss">
	.volume {
		display: flex;
		padding: 0;
    pointer-events: all;
	}
</style>
