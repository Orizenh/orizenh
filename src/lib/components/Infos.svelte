<script lang="ts">
    import logo from '$lib/assets/logo.svg'
    import { onMount } from 'svelte';
    import { fade } from 'svelte/transition';


    let showInfos:boolean = false

    onMount(() => {
        setTimeout(() => {
            showInfos = true
        }, 100)
    })

</script>

<svelte:head>
    <title>Orizenh | Présentation de l'entreprise</title>
    <meta name="description" content="Orizenh, c’est l’alliance entre performance, design soigné et développement zen. Fort de 10 ans d’expérience en développement web, je crée des sites modernes, rapides et 100 % adaptés à vos besoins. De la landing page percutante à l’application sur-mesure, chaque projet est conçu avec rigueur, simplicité… et élégance." />
</svelte:head>


{#if showInfos}
    <section class="orizenh-presentation" transition:fade={{duration:1000}}>
        <h2>
            Orizenh
        </h2>
        <p>
        <strong>Orizenh</strong>, c’est l’alliance entre performance, design soigné et développement zen.<br><br>
        Fort de <strong>10 ans d’expérience</strong> en développement web, je crée des sites modernes, rapides et 100 % adaptés à vos besoins. De la landing page percutante à l’application sur-mesure, chaque projet est conçu avec rigueur, simplicité… et élégance.
        </p>
    
        <h3>Mon objectif</h3>
        <p>
        Vous offrir un site <strong>clair, fluide et évolutif</strong>, qui vous ressemble et qui convertit efficacement.
        </p>
    
        <h3>Services proposés</h3>
        <ul>
        <li>Développement Front & Back (Svelte, React, Node.js...)</li>
        <li>Création de landing pages optimisées</li>
        <li>Intégration responsive & SEO friendly</li>
        <li>Déploiement, maintenance & optimisation continue</li>
        </ul>
        <p>
        Avec <strong>Orizenh</strong>, pas de stress : du code propre, une communication fluide et un projet livré avec le sourire.
        </p>
    </section>
    <img class="logo" src={logo} alt="Logo ORIZENH" />
{/if}

  <style>
    section{
        position: relative;
        color: var(--white);
        padding: 0 1rem;
        max-width: 75%;
        margin: auto;
        top: -50px;
    }
    section *{
        text-shadow: 0 0 10px var(--blue);
    }
    h2, h3{
        color: var(--blue);
        margin-top: 0;
    }
    p{
        margin-bottom: 3rem;
        font-size: 1.2rem;
    }
    ul li{
        font-size: 1.2rem;
    }
    img{
        position: absolute;
        bottom: 15px;
        right: 15px;
        opacity: 1;
    }
  </style>