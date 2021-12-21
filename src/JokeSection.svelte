<script>
    import Joke from "./Joke.svelte"
    import NextButton from "./NextButton.svelte"
    let nextJoke
</script>
<section class="section">
    <div class="section-joke">

                    <Joke bind:joke={nextJoke} />


                    <NextButton on:click={() => nextJoke.getJoke()}/>

    </div>
</section>
