<aside>
	<ul>
		<li>
			<a href="/">Home</a>
		</li>
		<li>
			<a href="/about">About</a>
		</li>
	</ul>
</aside>

<style>
	aside {
		display: flex;
		background-color: #f4f4f4;
        padding: 1rem 0.5rem;
	}

	aside ul {
        display: flex;
        list-style-type: none;
        writing-mode: vertical-lr;
        gap: 1rem;
	}

	aside li {
		display: flex;
		transform: rotate(180deg);
        font-weight: 500;
        font-size: 1.1rem;
	}

	aside a {
		display: inline-block;
		text-decoration: none;
		color: black;
	}
</style>
