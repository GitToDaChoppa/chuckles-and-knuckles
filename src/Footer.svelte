<script>
</script>


<footer class="footer has-background-dark is-bold">
    <div class="content has-text-centered has-text-white-ter">
        <p class="is-size-6">
            <a href="/">Svelte Norris</a> by <a href="https://www.brandonscrushy.com" >Brandon Scrushy</a>
        </p>
        <p>
            Made with <a href="https://svelte.dev"> Svelte</a> and the <a href="https://api.chucknorris.io/">Chuck Norris Jokes API</a>
        </p>
    </div>
</footer>

<style>
    footer {
        height: 30%;
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
/* 
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
    } */
</style>
