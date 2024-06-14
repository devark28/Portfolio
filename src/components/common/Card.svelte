<script lang="ts">
	export let primary: string;
	export let secondary: string;
	export let description: string | undefined = undefined;
</script>

<div class="card">
	<div class="heading" style="border-bottom-width: {description != undefined ? '1px' : '0px'};">
		<div class="icon">Icon</div>
		<div class="title">
			<div class="primary">{primary}</div>
			<div class="secondary">{secondary}</div>
		</div>
	</div>
	{#if description != undefined}
		<div class="description">{description}</div>
	{/if}
</div>

<style>
	.card {
		display: flex;
		flex-direction: column;
		background: #fd7d7d;
		width: 20rem;
		height: fit-content;
		/* max-height: 8rem; */
		color: #fff;
		padding: 1rem 2rem;
		gap: 1rem;
		border-radius: 0.4rem;
	}

	.heading {
		display: flex;
		border-bottom-width: 0px;
		border-bottom-style: solid;
		border-bottom-color: white;
		padding: 0.4rem 0rem;
		gap: 0.5rem;
	}

	.icon {
		display: flex;
		justify-content: center;
		align-items: center;
		width: 4rem;
		height: 4rem;
		background: hsla(0, 0%, 100%, 0.2);
		border-radius: 0.3rem;
	}

	.title {
		display: flex;
		flex-direction: column;
	}

	.primary {
		font-size: 2rem;
	}

	.secondary {
		font-size: 0.7rem;
	}

	.description {
		font-size: 1rem;
	}
</style>
