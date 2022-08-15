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
		width: 50px;
		height: 50px;
		display: flex;
		border-radius: 50%;
		padding: 0;
    pointer-events: all;
	}
</style>
