<script>
	import SwatchList from './components/SwatchList.svelte'
</script>

<main>
	<section>
		<h1>Color Palette</h1>
	</section>
		
	<SwatchList />
</main>

<style lang="scss">
	h1, h2 {
		font-weight: 700;
	}

	h1 {
		font-size: 2rem;
	}
	
	h2 {
		font-size: 1.5rem;
	}
	
	main {
		text-align: left;
		padding: 4em;
		margin: 0 auto;
	}

	section {
		margin-bottom: 4rem;
	}

	ul {
		list-style: none;
		margin: 0;
		padding: 0;
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		gap: 1rem;
	}

	li:not(:last-child) {
		margin-bottom: .25rem;
	}

	code {
		font-family: inherit;
		font-weight: 600;
		color: #3B4549;
		padding: .125rem .25rem;
		background: #F5F8FA;
		border-radius: .25rem;
	}

	a {
		font-weight: 500;
		color: #6F3C94;
		padding: .125rem .25rem;
		background: #F9EDFF;
		border-radius: .25rem;
		
		&:hover {
			color: #6F3C94;
		}
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>