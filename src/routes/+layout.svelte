<script lang="ts">
	import '../css/global.css';
	import Nav from '../components/Nav.svelte';
	import Footer from '../components/Footer.svelte';
</script>

<div class="app" style="overflow: hidden;">
	<Nav />

	<div class="app-content">
		<main>
			<slot />
		</main>

		<Footer />
	</div>
</div>

<style>
	.app {
		display: flex;
		height: 100vh;
		width: 100vw;
	}

	.app-content {
		display: flex;
		flex-direction: column;
		flex: 1;
		height: inherit;
	}

	main {
		display: flex;
		flex: 1;
		width: 100%;
	}
</style>
