<script>

</script>

<div class="container">
        <button class="button is-danger is-bold has-text-weight-bold is-size-5" on:click>
            <span class="fist-pump">👊</span><span class="next">HIT ME</span>
        </button>
</div>


<style>
    .container {
        display: flex;
        flex-wrap: nowrap;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        height: 10vh;
    }
    button {
        border-radius: 7px !important;
        box-shadow: 0 3px 5px 0 rgba(0,0,0,0.3);
        transform: scale(1);
    }

    button:active {
        transform: scale(0.9);
        background-color: #33332f !important;
    }

    .fist-pump {
        animation: pump .5s ease infinite alternate;
    }
    .next {
        padding-left: 6px;
    }
    @keyframes pump {
        0% {transform: scale(1)}
        100% {transform: scale(1.4)}
    }
</style>