<script lang="ts">
	import { page } from '$app/stores';

	$: pathname = $page.route.id;
</script>

<aside>
	<ul>
		<li data-active={pathname == '/' ? 'true' : 'false'}>
			<a href="/">Home</a>
		</li>
		<li data-active={pathname == '/skills' ? 'true' : 'false'}>
			<a href="/skills">Skills</a>
		</li>
		<li data-active={pathname == '/experience' ? 'true' : 'false'}>
			<a href="/experience">Experience</a>
		</li>
		<li data-active={pathname == '/contact' ? 'true' : 'false'}>
			<a href="/contact">Contact</a>
		</li>
	</ul>
</aside>

<style>
	aside {
		display: flex;
		background-color: #f4f4f4;
		padding: 1.5rem 1rem;
	}

	aside ul {
		display: flex;
		list-style-type: none;
		writing-mode: vertical-lr;
		gap: 2rem;
	}

	aside li {
		display: flex;
		transform: rotate(180deg);
		font-weight: 600;
		font-size: 1.05rem;
		position: relative;
		cursor: pointer;
		color: black;
		transition: color 0.2s;
	}

	aside li:hover,
	aside li[data-active='true'] {
		color: #fd7d7d;
	}

	aside li::before {
		content: '';
		display: block;
		width: 100%;
		height: 0;
		border-radius: 0.3rem;
		position: absolute;
		top: -0.7rem;
		transition: height 0.3s;
	}

	aside li[data-active='true']::before {
		height: 0.25rem;
		background-color: #fd7d7d;
	}

	aside a {
		display: inline-block;
		text-decoration: none;
		color: inherit;
	}
</style>
