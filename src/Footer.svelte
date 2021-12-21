<script>
</script>


<section class="section">
    <footer class="footer has-background-dark is-bold">
        <div class="content has-text-centered has-text-white-ter">
            <p class="is-size-6">
                <a href="/">Svelte Norris</a> © 2021 <a href="https://www.brandonscrushy.com" >Brandon Scrushy</a>
            </p>
            <p>
                Made with <a href="https://svelte.dev"> Svelte</a>. Jokes are from the <a href="https://api.chucknorris.io/">Chuck Norris Jokes API.</a>
            </p>
            <img class="bounce" src="https://res.cloudinary.com/bokbok/image/upload/v1636490946/brando/brando-2022_j3g7zm.png" alt="brando is happy" width="64px"/>
        </div>
    </footer>
</section>

<style>
	    /* footer {
        height: 30%;
        bottom: 0;
    } */

    section {
        bottom: 0
    }
    
    a {
        color: #c3c3c3;
        font-weight: bold;
    }

    a:hover {
        color: gray;
        text-decoration: none !important;
    }

    a:active {
        color: #8c1313;
        font-size: 95%;
        text-decoration: none !important;
    }

    .bounce {
        animation: brando-bounce 1s ease infinite alternate;
    }

    @keyframes brando-bounce {
        0% {
            transform: translateY(0) scale(1)
        }
        100% {
            transform: translateY(16px) scale(1.25)
        }
    }
</style>
