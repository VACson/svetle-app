<script>
  import Vintage from '../assets/clients/Vintage.svelte';
  import Violet from '../assets/clients/Violet.svelte';
  import Ceathes from '../assets/clients/Ceathes.svelte';
  import CreaterFav from '../assets/clients/CreaterFav.svelte';
  import LavenderAgency from '../assets/clients/LavenderAgency.svelte';
  const clientsIcons = [Vintage, Violet, Ceathes, CreaterFav, LavenderAgency];
</script>

<section class="clients">
  <h2 class="heading-2 font-inter">Our Clients</h2>
  <p class="paragraph">We have worked with great clients for which we are very proud.</p>
  <div class="clients__jumbotron">
    {#each clientsIcons as clientIcon}
      <a href="/" class="clients__jumbotron__img">
        <svelte:component this={clientIcon} />
      </a>
    {/each}
  </div>
</section>

<style>
  @media (max-width: 1200px) {
    .clients {
      width: 100%;
      height: fit-content;
      padding: 50px;
    }
    .clients__jumbotron {
      margin: 50px 0;
      display: flex;
      flex-flow: row wrap;
      justify-content: center;
      gap: 50px;
    }
  }
</style>