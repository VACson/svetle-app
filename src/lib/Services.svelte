<script>
  import { servicesData } from './servicesData';
</script>

<section class="services__section">
  <div class="services__title">
    <h2 class="heading-2 font-inter">Our Services</h2>
    <p class="services__title__caption paragraph">
      Voluptas sit aspernatur te natus accusan maiores alias consequatur aut equatur aut perferendi.
    </p>
  </div>
  <div class="services__container">
    {#each servicesData as service}
      <div class="services__container__item">
        <div class="services__icon">
          <svelte:component this={service.Icon} />
        </div>
        <h3 class="heading-3 font-inter">{service.title}</h3>
        <p class="paragraph">{service.content}</p>
      </div>
    {/each}
  </div>
</section>

<style>
  @media (max-width: 1200px) {
    .services__section {
    height: fit-content;
  }
  .services__title {
    width: 100%;
  }
  .services__container {
    display: flex;
    flex-flow: column nowrap;
  }
  .services__container__item {
    width: 100%;
  }
  }
</style>
