<script lang="ts">
	import Viewport from '../components/common/Viewport.svelte';
</script>

<Viewport>
	<div class="container">
		<div class="text">
			<div class="content">
				<div class="primary">Bruce SHIMWA Emmanuel</div>
				<div class="secondary">A modern and experienced developer aiming at improving the User Experience</div>
				<div class="cta">
					<button><a href="/skills">Discover My Skills</a></button>
				</div>
			</div>
		</div>
		<div class="image">
			<img src="https://via.placeholder.com/270" alt="placeholder" />
		</div>
	</div>
</Viewport>

<style>
	.container {
		display: flex;
		flex: 1;
		justify-content: center;
		align-items: center;
		height: 100%;
		width: 100%;
		padding: 0 1rem;
	}

	.text {
		display: flex;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

	.content {
		display: flex;
		flex-direction: column;
		max-width: 30rem;
		gap: .5rem;
	}

	.primary {
		font-size: 2rem;
	}

	.secondary {
		font-size: 1rem;
	}

	.cta {
		margin-top: 1rem;
	}

	.cta button {
		background-color: #fd7d7d;
		color: #fff;
		padding: 0.7rem 1.2rem;
		border: none;
		border-radius: 0.25rem;
	}

	.cta button a {
		color: inherit;
		text-decoration: none;
	}

	.image {
		display: flex;
		justify-content: center;
		align-items: center;
		flex: 1;
	}
</style>
