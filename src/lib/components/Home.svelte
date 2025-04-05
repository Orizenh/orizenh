<script lang="ts">
    import { onMount } from "svelte";
    import logo_inline from '$lib/assets/logo_inline.svg'
    import { fade } from "svelte/transition";

    let showLogo:boolean = false

    onMount(() => {
        setTimeout(() => {
            showLogo = true
        }, 100)
    })
</script>


<svelte:head>
    <title>Orizenh</title>
    <meta name="description" content="Orizenh - Développement web moderne et performant" />
</svelte:head>

{#if showLogo}
    <img class="logo" 
    src={logo_inline} 
    alt="Logo ORIZENH" 
    transition:fade={{duration:1000}} />
{/if}

<style>
    @media (max-width: 991px) {
        .logo{
        width: 90%;
        }
    }
    img{
        margin: auto;
        width: 50%;
    }
</style>