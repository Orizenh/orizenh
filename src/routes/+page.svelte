<script>
    import { view } from '$lib'
    import Footer from '$lib/components/Footer.svelte';
    import Infos from '$lib/components/Infos.svelte';
    import Home from '$lib/components/Home.svelte';
    import Animation from '$lib/components/Animation.svelte';
</script>

<main>
  {#if $view === "default"}
      <Home />
  {:else if $view === "infos"}
      <Infos />
  {/if}
  <Footer />
  <Animation />
</main>

<style> 
  main{
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      height: 100vh;
  }
</style>