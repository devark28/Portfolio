<script lang="ts">
	import '../../css/global.css';
	import { spring } from 'svelte/motion';
	import { onMount } from 'svelte';

	// scale from 0.7 to 1, translateY from -0.7 to 0, opacity from 0 to 1, with a duration of 400ms
	$: scale = spring(1.2);
	$: translateY = spring(0.5);
	$: opacity = spring(0);
	$: blur = spring(3);

	onMount(() => {
		scale.set(1);
		translateY.set(0);
		opacity.set(1);
		blur.set(0);
	});
</script>

<div class="base-viewport">
	<div
		class="viewport"
		style="transform: scale({$scale * 100}%) translateY({$translateY *
			100}%); opacity: {$opacity}; filter: blur({$blur}px);"
	>
		<slot />
	</div>
</div>

<style>
	.base-viewport {
		display: flex;
		flex: 1;
		width: 100%;
		position: relative;
	}

	.viewport {
		display: flex;
		flex-direction: column;
		height: inherit;
		background-color: #fbe1e1;
		width: 100%;
		height: 100%;
		position: absolute;
		transition:
			filter 1s,
			transform 1.5s,
			opacity 2s;
		transform-origin: center;

		/* box-shadow: -10px 10px 15px -20px black;
		border-bottom-left-radius: 1.5rem; */
	}
</style>
