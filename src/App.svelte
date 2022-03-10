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
                        <div class="level">
                          <div class="container px-4 py-2"></div>
                                      <Joke bind:joke={nextJoke} />
                                    </div>
	</main>
          	<NextButton on:click={() => nextJoke.getJoke()} />


	<!-- <Footer /> -->

</body>

<style>

		:global(*) {
			/* box-sizing: border-box; */
			font-family: 'Roboto', sans-serif;
			font-size: 16px;
		}


    main {
    margin: 0;
		padding: 2em 4em 2em 4em;
		display: flex;
		height: 69vh;
		flex-direction: column;
		flex-wrap: wrap;
		align-items: center;
		justify-content: center;
    overflow-y: hidden;
    }
</style>
