<script>
    import { onMount } from 'svelte';

    onMount(() => {
        const navEl = document.getElementsByTagName("nav")[0];
        window.onscroll = () => {
            if ((document.body.scrollTop || document.documentElement.scrollTop) > 0)
                navEl.style.transform = "translateY(-100%)";
            else
                navEl.style.transform = "translateY(0%)";
        }
    });
</script>

<nav>
    <img src="/src/assets/logo_banner.png" alt="logo_banner">
    <div class="flex-spacer"></div>
    <a href="/about">About</a>
    <a href="/resources">Resources</a>
    <a href="/partners">Partnerships</a>
    <a href="/join">Join Us</a>
    <a href="/news">News</a>
</nav>

<style>
    nav {
        position: absolute;
        width: 100%;
        background: white;
        border-bottom: 2px solid #dee2e6; 
        display: flex;
        flex-direction: row;
        transition: transform 0.5s;
    }
    nav > img {
        max-height: 50px;
        padding-top: 0.5rem;
        padding-bottom: 0.5rem;
        padding-left: 1rem;
        padding-right: 1rem;
    }
    nav > a {
        position: relative;
        padding-top: 0.75rem;
        padding-bottom: 0.75rem;
        padding-left: 1rem;
        padding-right: 1rem;
    }
    nav > a::after {
        content: '';
        position: absolute;
        bottom: 0.5rem;
        left: 50%;
        transform: translateX(-50%);
        width: 0%;
        transition: width 0.4s;
        height: 2px;
        background: red;
        z-index: 1;
    }
    nav > a:hover::after {
        width: calc(100% - 2rem);
    }
    .flex-spacer {
        flex-grow: 1;
    }
</style>