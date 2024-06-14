<script lang="ts">
	import Card from '../../components/common/Card.svelte';
	import Viewport from '../../components/common/Viewport.svelte';
	const myExperience = [{ title: 'HTML', company: 'Byimana School', period: '1 year' }];
</script>

<Viewport>
	<div class="container">
		<div class="heading">Skills</div>
		<div class="cards">
			{#each myExperience as experience}
				<Card
					primary={experience.title}
					secondary={experience.period}
					description={experience.company}
				/>
			{/each}
		</div>
	</div>
</Viewport>

<style>
	.container {
		display: flex;
		flex: 1;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height: 100%;
		width: 100%;
	}

	.heading {
		display: flex;
		justify-content: center;
		align-items: center;
		width: 100%;
		font-size: 1.5rem;
		padding: 1rem 4rem;
	}

	.cards {
		display: flex;
		flex: 1;
		flex-flow: wrap;
		justify-content: center;
		width: 100%;
		padding: 2rem 4rem;
		gap: 1.3rem;
		overflow: auto;
	}
</style>
