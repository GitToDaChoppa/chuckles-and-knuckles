<script>
	import Footer from "./Footer.svelte"
	import Hero from "./Hero.svelte"
	import JokeSection from "./JokeSection.svelte"



</script>

	<main>
		<Hero />
		<JokeSection />
		<Footer />
	</main>



<style>
main {
	 height: 100vh;
	 min-height: 100vh;
 }


:global(footer) {
	bottom: 0;
	align-self: end;
}
</style>
<!-- <style>

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
		/* height: 50vh; */
		flex-direction: column;
		/* flex-wrap: wrap; */
		align-items: center;
		justify-content: space-between;
    }
</style> -->
