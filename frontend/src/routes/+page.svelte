<script>
    import S1 from '$lib/index/S1.svelte'
    import Cards from '$lib/index/Cards.svelte'
    // import S3 from '$lib/index/S3.svelte'
    // import S4 from '$lib/index/S4.svelte'
</script>

<main>
    <S1></S1>
    <Cards></Cards>
    <!-- <S3></S3>
    <S4></S4> -->
    <section id="s3" class="redir">
        <div id="about_us">
            <div>
                <h1>About Us</h1>
                <p>There is no organization without its team. Let's meet those that are behind the curtain.</p>
                <button type="button">Learn More</button>
            </div>
            <img src="/src/assets/index/about_us.png">
            <!-- <div><div style="width: 200px; height: 300px; background: red;"></div></div> -->
        </div>
    </section>
    <section id="s4" class="redir">
        <div id="resources">
            <img src="/src/assets/index/resources.png">
            <div>
                <h1>Resources</h1>
                <p>We offer many educational and support resources to help you grow!</p>
                <button type="button">Look Up</button>
            </div>
        </div>
    </section>
    <section id="s5" class="redir">
        <div id="partners">
            <div>
                <h1>Partners</h1>
                <p>We work with organizations and people from all around the world to reach our mission.</p>
                <button type="button">Read More</button>
            </div>
            <img src="/src/assets/index/partners.png">
        </div>
    </section>
    <section id="s6" class="redir">
        <div id="join_in">
            <img src="/src/assets/index/join_in.png">
            <div>
                <h1>Join In</h1>
                <p>We have tons of opportunities at CTD for everyone!</p>
                <button type="button">Join Us</button>
            </div>
        </div>
    </section>
</main>

<style>
    :global(body) {
        background-repeat: no-repeat;
        background-attachment: fixed;
        background-size: cover;
        color: black;
        background-image: url("/src/assets/index/bg.png");
    }
    main {
        /* opacity: 0; */
        animation: fadein 1s ease;
    }
    @keyframes fadein {
        from {
            opacity: 0;
        }
        to {
            opacity: 1;
        }
    }
    .redir {
        position: relative;
        margin: 10vh 0;
    }
    .redir > div {
        display: grid;
        grid-auto-columns: 1fr;
        grid-column-gap: 16px;
        grid-row-gap: 16px;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: auto;
        margin: 0 auto;
    }
    .redir:nth-of-type(2n+1) > div > div:nth-child(1),
    .redir:nth-of-type(2n) > div > div:nth-child(2) {
        max-width: 20rem;
        display: flex;
        flex-direction: column;
        place-items: center;
        justify-content: center;
    }
    .redir > div > div > h1 {
        font-size: 32px;
        font-weight: 700;
    }
    .redir > div > div > button {
        color: white;
        font-weight: 900;
        padding: 0.5em 1em;
        border-radius: 100vmax;
    }
    #about_us > div > button {
        background-color: blue;
    }
    #resources > div > button {
        background-color: palevioletred;
    }
    #partners > div > button {
        background-color: blueviolet;
    }
    #join_in > div > button {
        background-color: purple;
    }
    .redir > div > img {
        height: 20rem;
    }
    .redir > div > div:first-child,
    .redir > div > img:first-child {
        margin-left: auto;
    }
    /* .redir::before {
        content: '';
        z-index: -1;
        position: absolute;
        inset: 0;
        background-color: #fff;
        opacity: 0.65;
    } */
</style>