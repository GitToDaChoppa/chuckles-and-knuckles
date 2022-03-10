<script>
    import {Shadow} from 'svelte-loading-spinners'
    import {onMount} from 'svelte'

    let result

    export const joke = {

        getJoke()
    {
        result = getResult()
    }

    }
        async function getResult() {
            let response = await fetch('https://api.chucknorris.io/jokes/random', {
                method: 'GET'
            })
            return await response.json();
        }

    onMount(() => {
        joke.getJoke()
    })

</script>

<div id="joke-container" class="px-4 py-2">
        {#if result===undefined }

            <p>Chuck Norris visited the site and... it broke. (This is not a joke, it's an error) 😔</p>

        {:else}

            {#await result}

                <Shadow size="80" color="#D9514E" unit="px" />

            {:then result}
                        <span class="the-joke is-unselectable">{result.value}</span>

            {:catch error}

                <p class="error-message">{error.message}</p>

            {/await}

        {/if}

</div>

<style>
  #joke-container {
    overflow: clip;
  }
    .the-joke {
        font-family: 'East Sea Dokdo', cursive !important;
        /* font-size: 3.25em;
        font-size: clamp(2rem, -0.875rem + 8.333vw, 5rem); */
        font-size: calc(3vw + 3vh + 1vmin);
        word-wrap: normal;
        /* word-break: break-all; */
        line-height: 0.8;
        overflow: hidden;
    }
    p {
        text-align: center;
        font-weight: normal;
    }

    p:not(.the-joke) {
        font-size: 2rem
    }

</style>