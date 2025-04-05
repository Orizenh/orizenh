<script lang="ts">
    import { activeItem } from "$lib"
    import logo_inline from '$lib/assets/logo_inline.svg'

    let items:Object = {
        "/":"Qui sommes-nous ?",
        "/contact": "Demande de devis"
    }

    $effect(() => {
        console.log($activeItem)
    })

</script>

<nav>
    <div class="flex">
        <a href="">
            <img class="logo" src='{logo_inline}' alt="Logo ORIZENH" />
        </a>
        <ul class="flex">
            {#each Object.entries(items) as [href,label]}
            <li>
                <a {href} 
                class:active={href === $activeItem} 
                onclick={() => $activeItem = href}>
                    {label}
                </a>
            </li>
            {/each}
        </ul>
    </div>
    <div class="flex socials">
        <a href="https://www.linkedin.com/in/gwena%C3%ABl-pigat-a95a58aa/" target="_blank" 
    aria-label="Compte LinkedIN">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512" class="svelte-yx20j"><path d="M416 32H31.9C14.3 32 0 46.5 0 64.3v383.4C0 465.5 14.3 480 31.9 480H416c17.6 0 32-14.5 32-32.3V64.3c0-17.8-14.4-32.3-32-32.3zM135.4 416H69V202.2h66.5V416zm-33.2-243c-21.3 0-38.5-17.3-38.5-38.5S80.9 96 102.2 96c21.2 0 38.5 17.3 38.5 38.5 0 21.3-17.2 38.5-38.5 38.5zm282.1 243h-66.4V312c0-24.8-.5-56.7-34.5-56.7-34.6 0-39.9 27-39.9 54.9V416h-66.4V202.2h63.7v29.2h.9c8.9-16.8 30.6-34.5 62.9-34.5 67.2 0 79.7 44.3 79.7 101.9V416z"></path></svg>
        </a>
        <a href="mailto:gwenael.pigat@gmail.com" 
        aria-label="Envoyer un mail">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" class="svelte-yx20j"><path d="M48 64C21.5 64 0 85.5 0 112c0 15.1 7.1 29.3 19.2 38.4L236.8 313.6c11.4 8.5 27 8.5 38.4 0L492.8 150.4c12.1-9.1 19.2-23.3 19.2-38.4c0-26.5-21.5-48-48-48L48 64zM0 176L0 384c0 35.3 28.7 64 64 64l384 0c35.3 0 64-28.7 64-64l0-208L294.4 339.2c-22.8 17.1-54 17.1-76.8 0L0 176z"></path></svg>
        </a>
        <a href="https://toolsbox.ferox-portal.com" 
        target="_blank" 
        aria-label="Outils en ligne">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 512" class="svelte-yx20j"><path d="M392.8 1.2c-17-4.9-34.7 5-39.6 22l-128 448c-4.9 17 5 34.7 22 39.6s34.7-5 39.6-22l128-448c4.9-17-5-34.7-22-39.6zm80.6 120.1c-12.5 12.5-12.5 32.8 0 45.3L562.7 256l-89.4 89.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0l112-112c12.5-12.5 12.5-32.8 0-45.3l-112-112c-12.5-12.5-32.8-12.5-45.3 0zm-306.7 0c-12.5-12.5-32.8-12.5-45.3 0l-112 112c-12.5 12.5-12.5 32.8 0 45.3l112 112c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L77.3 256l89.4-89.4c12.5-12.5 12.5-32.8 0-45.3z"></path></svg>
        </a>
    </div>

</nav>

<style>
    .logo{
        margin-right: 2rem;
        margin-top: 0.5rem;
    }
    .flex{
        display: flex;
        align-items: center;
    }
    .socials a{
        color: var(--white);
        display: inline-flex;
        align-items: center;
        justify-content: center;
        margin: 0 0.5rem;
        transition-duration: .4s;
    }
    .socials a:hover{
        transform: scale(1.2);
        transition-duration: .4s;
    }
    .socials a:hover svg{
        transition-duration: .4s;
        fill: var(--purple);
    }
    .socials a svg{
        fill: var(--white);
        width: 30px;
        height: 30px;
        transition-duration: .4s;
    }

    nav{
        max-height: 45px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 1.5rem 0;
        color: var(--white);
        background-color: var(--black);
        box-shadow: 0 0 10px 0px var(--black);
        position: fixed;
        top: 0;
        left: 0;
        width: -webkit-fill-available;
    }
    nav ul{
        padding: 0;
        margin: 0;
    }
    nav ul li{
        list-style-type: none;
        display: inline-block;
    }
    nav ul li a{
        padding: 1rem;
        text-decoration: none;
        font-size: 1.3rem;
        color: var(--white);
        transition-duration: .4s;
    }
    nav ul li a:hover,.active{
        color: var(--blue);
        transition-duration: .4s;
    }
    nav ul li:first-child a{
        margin-left: 0;
    }
</style>