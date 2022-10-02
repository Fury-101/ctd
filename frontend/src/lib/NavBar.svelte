<script>
    import { onMount } from 'svelte';

    onMount(() => {
        const navEl = document.getElementsByTagName("nav")[0];
        document.addEventListener('scroll', () => {
            if ((document.body.scrollTop || document.documentElement.scrollTop) > 0)
                navEl.style.transform = "translateY(-100%)";
            else
                navEl.style.transform = "translateY(0%)";
        });
    });
</script>

<nav>
    <img src="/src/assets/logo_banner.png" alt="logo_banner">
    <a href="/about">About</a>
    <a href="/resources">Resources</a>
    <a href="/partners">Partnerships</a>
    <a href="/join">Join Us</a>
    <a href="/news">News</a>
</nav>

<style>
    nav {
        z-index: 1;
        position: absolute;
        width: 100%;
        background: white;
        border-bottom: 2px solid #dee2e6; 
        display: flex;
        flex-direction: row;
        place-items: center;
        transition: transform 0.5s;
        animation: slidein 0.5s;
    }
    @keyframes slidein {
        from {
            transform: translateY(-100%);
        }
        to {
            transform: translateY(0%);
        }
    }
    nav > img {
        max-height: 64px;
        padding-top: 0.5rem;
        padding-bottom: 0.5rem;
        padding-left: 1rem;
        padding-right: 1rem;
    }
    nav > a {
        color: black;
        position: relative;
        padding-top: 0.75rem;
        padding-bottom: 0.75rem;
        padding-left: 1rem;
        padding-right: 1rem;
    }
    nav > a:first-of-type {
        margin-left: auto;
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
        background: var(--primary);
        z-index: 1;
    }
    nav > a:hover::after {
        width: calc(100% - 2rem);
    }
</style>