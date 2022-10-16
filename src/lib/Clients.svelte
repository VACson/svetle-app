<script>
  import Vintage from '../assets/clients/Vintage.svg';
  import Violet from '../assets/clients/Violet.svg';
  import Ceathes from '../assets/clients/Ceathes.svg';
  import CreaterFav from '../assets/clients/CreaterFav.svg';
  import LavenderAgency from '../assets/clients/LavenderAgency.svg';
  const clientsIcons = [Vintage, Violet, Ceathes, CreaterFav, LavenderAgency];
</script>

<section class="clients">
  <h2>Our Clients</h2>
  <p>We have worked with great clients for which we are very proud.</p>
  <div class="clients__jumbotron">
    {#each clientsIcons as clientIcon}
      <img src={clientIcon} class="clients__jumbotron__img" alt="" />
    {/each}
  </div>
</section>
