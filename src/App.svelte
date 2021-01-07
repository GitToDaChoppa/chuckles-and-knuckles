<script>
	import Joke from './Joke.svelte'
	import Footer from "./Footer.svelte"
	import Hero from "./Hero.svelte"
	import NextButton from "./NextButton.svelte"

	let nextJoke

</script>

<body>

	<Hero />

	<main>

			<div class="columns">
				<div class="column">
					<Joke bind:joke={nextJoke} />
				</div>
			</div>

	</main>

	<NextButton on:click={() => nextJoke.getJoke()} />

	<Footer />

</body>

<style>

		:global(*) {
			box-sizing: border-box;
			font-family: 'Roboto', sans-serif;
			font-size: 16px;
		}


@media only screen and (min-width:660px) and (min-height: 700px) {
	body {
		overflow: hidden;
	}
}

		@media only screen and (max-width: 600px) {
		:global(*) {
			font-size: 12px;
		}
	}

    main {
        margin: 0;
		padding: 8px;
		display: flex;
		height: 50vh;
		flex-direction: column;
		flex-wrap: wrap;
		align-items: center;
		justify-content: center;
    }
</style>
