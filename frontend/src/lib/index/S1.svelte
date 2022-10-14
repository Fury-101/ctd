<section id="s1">
    <!-- <div id="banner_container">
        <video autoplay loop muted inline>
            <source src="/src/assets/index/banner.mp4" type="video/mp4">
        </video>
    </div> -->
    <div id="text">
        <h1>Closing The Divide</h1>
        <h2>Dedicated to increasing technological literacy for low-income families.</h2>
    </div>
</section>

<style>
    #s1 {
        height: 100vh;
    }
    #s1 > #text {
        font-size: 5vw;
        font-weight: 500;
        padding-top: calc(50vh - calc(2 * 1em));
        padding-left: 32px;
        transform: translateX(-100%);
        animation: flyin ease-out 1.5s 1 normal forwards;
    }
    @keyframes flyin {
        from {
            transform: rotateX(360deg) translateX(-100%);
        }
        to {
            transform: rotateX(0);
        }
    }
    #s1 > div > h2 {
        font-size: 2.5vw;
        width: 75vw;
    }
</style>