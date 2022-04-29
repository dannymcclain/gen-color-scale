<script>
	import SwatchList from './components/SwatchList.svelte'
</script>

<main>
	<h1>Generated color scale</h1>
	<p style="margin-bottom: 4rem;">I plugged some hand-picked swatch colors (the 500's) into <a href="https://hihayk.github.io/scale/#4/6/50/80/-51/67/20/14/1D9A6C/29/154/108/white">Scale</a> to generate the rest of the palette.</p>
	<SwatchList />
</main>

<style lang="scss">
	main {
		text-align: left;
		padding: 4em;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>