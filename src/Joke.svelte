<script>
    import {Shadow} from 'svelte-loading-spinners'
    import {onMount} from 'svelte'

    let query = ''
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

<div>
        {#if result===undefined }

            <p>Chuck Norris visited the site and... it broke. (This is not a joke, it's an error)</p>

        {:else}

            {#await result}

                <Shadow size="80" color="#D9514E" unit="px" />

            {:then result}
                        <p class="the-joke">{result.value}</p>

            {:catch error}

                <p class="error-message">{error.message}</p>

            {/await}

        {/if}

</div>

<style>
☺♂◘
    .the-joke {
        font-family: 'East Sea Dokdo', cursive !important;
        font-size: 3rem;
    }
    p {
        text-align: center;
        font-weight: normal;
    }

    p:not(.the-joke) {
        font-size: 2rem
    }

</style>