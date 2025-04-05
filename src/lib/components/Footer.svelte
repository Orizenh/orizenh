<script>
    import { onMount } from "svelte";
    import { fade } from "svelte/transition";
    import { view } from '$lib'

    let showFooter = false

    onMount(() => {
        setTimeout(() => {
            showFooter = true
        }, 2000)
    })
    
</script>


{#if showFooter}
<footer transition:fade={{duration:1000}}>
    {#if $view === "default"}
        <button class="item" 
        aria-label="Qui sommes-nous ?"
        onclick={() => { view.set("infos") }}>
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path d="M256 512A256 256 0 1 0 256 0a256 256 0 1 0 0 512zM169.8 165.3c7.9-22.3 29.1-37.3 52.8-37.3l58.3 0c34.9 0 63.1 28.3 63.1 63.1c0 22.6-12.1 43.5-31.7 54.8L280 264.4c-.2 13-10.9 23.6-24 23.6c-13.3 0-24-10.7-24-24l0-13.5c0-8.6 4.6-16.5 12.1-20.8l44.3-25.4c4.7-2.7 7.6-7.7 7.6-13.1c0-8.4-6.8-15.1-15.1-15.1l-58.3 0c-3.4 0-6.4 2.1-7.5 5.3l-.4 1.2c-4.4 12.5-18.2 19-30.6 14.6s-19-18.2-14.6-30.6l.4-1.2zM224 352a32 32 0 1 1 64 0 32 32 0 1 1 -64 0z"/></svg>
        </button>
    {:else}
        <button class="item" 
        aria-label="Retour à l'accueil"
        onclick={() => { view.set("default") }}>
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path d="M9.4 233.4c-12.5 12.5-12.5 32.8 0 45.3l160 160c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L109.2 288 416 288c17.7 0 32-14.3 32-32s-14.3-32-32-32l-306.7 0L214.6 118.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-160 160z"/></svg>
        </button>
    {/if}
    <a href="https://www.linkedin.com/in/gwena%C3%ABl-pigat-a95a58aa/" target="_blank" 
    aria-label="Compte LinkedIN" 
    class="item">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512" ><path d="M416 32H31.9C14.3 32 0 46.5 0 64.3v383.4C0 465.5 14.3 480 31.9 480H416c17.6 0 32-14.5 32-32.3V64.3c0-17.8-14.4-32.3-32-32.3zM135.4 416H69V202.2h66.5V416zm-33.2-243c-21.3 0-38.5-17.3-38.5-38.5S80.9 96 102.2 96c21.2 0 38.5 17.3 38.5 38.5 0 21.3-17.2 38.5-38.5 38.5zm282.1 243h-66.4V312c0-24.8-.5-56.7-34.5-56.7-34.6 0-39.9 27-39.9 54.9V416h-66.4V202.2h63.7v29.2h.9c8.9-16.8 30.6-34.5 62.9-34.5 67.2 0 79.7 44.3 79.7 101.9V416z"></path></svg>
    </a>
    <a href="mailto:orizenhcontact001@gmail.com" 
    aria-label="Envoyer un mail" 
    class="item">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" ><path d="M48 64C21.5 64 0 85.5 0 112c0 15.1 7.1 29.3 19.2 38.4L236.8 313.6c11.4 8.5 27 8.5 38.4 0L492.8 150.4c12.1-9.1 19.2-23.3 19.2-38.4c0-26.5-21.5-48-48-48L48 64zM0 176L0 384c0 35.3 28.7 64 64 64l384 0c35.3 0 64-28.7 64-64l0-208L294.4 339.2c-22.8 17.1-54 17.1-76.8 0L0 176z"></path></svg>
    </a>
    <a href="https://toolsbox.ferox-portal.com" 
    target="_blank" 
    class="item"
    aria-label="Outils en ligne">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 512" ><path d="M392.8 1.2c-17-4.9-34.7 5-39.6 22l-128 448c-4.9 17 5 34.7 22 39.6s34.7-5 39.6-22l128-448c4.9-17-5-34.7-22-39.6zm80.6 120.1c-12.5 12.5-12.5 32.8 0 45.3L562.7 256l-89.4 89.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0l112-112c12.5-12.5 12.5-32.8 0-45.3l-112-112c-12.5-12.5-32.8-12.5-45.3 0zm-306.7 0c-12.5-12.5-32.8-12.5-45.3 0l-112 112c-12.5 12.5-12.5 32.8 0 45.3l112 112c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L77.3 256l89.4-89.4c12.5-12.5 12.5-32.8 0-45.3z"></path></svg>
    </a>
    <p>© {new Date().getFullYear()} - Gwenaël Pigat</p>
</footer>
{/if}

<style>
    @media (max-width: 991px) {
        footer{
            background-color: var(--black);
        }
    }
    footer{
        position: fixed;
        bottom: 0;
        left: 0;
        right: 0;
        padding: 1rem;
        text-align: center;
    }
    footer .item{
        margin: 0 0.5rem;
        display: inline-flex;
        align-items: center;
        justify-content: center;
        border: 0;
        background: transparent;
        padding: 0;
    }
    footer .item:hover{
        cursor: pointer;
    }
    footer .item svg{
        fill: var(--purple);
        width: 30px;
        height: 30px;
        transition-duration: .4s;
    }
    footer .item:hover svg{
        fill: var(--blue);
        transform: scale(1.2);
    }
    footer p{
        display: flex;
        align-items: center;
        justify-content: center;
        margin: .5rem 0 0;
        color: var(--purple);
        text-shadow: 0 0 5px var(--purple);
    }
</style>