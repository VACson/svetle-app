<script>
  import Ui from '../assets/services/Ui.svg';
  import Branding from '../assets/services/Branding.svg';
  import Design from '../assets/services/Design.svg';
  let services = [
    {
      img: Ui,
      name: 'UI/UX Design',
      p: 'Perferendis doloribus asperiores repellat quia voluptas aspernatur te natus accusan maiores        alias consequatur aut aut.',
    },
    {
      img: Branding,
      name: 'Branding',
      p: 'Asperiores repellat quia voluptas aut aspernatur te natus accusan maiores alias consequatur aut perferendis dolor.',
    },
    {
      img: Design,
      name: 'Logo Design',
      p: 'Maiores alias consequatur aut aut repellat perferendi doloribus asperiores voluptas aspernatur te natus accusan.',
    },
  ];
</script>
<section class="services__section">
  <div class="services__title">
    <h2>Our Services</h2>
    <p class="services__title__caption">
      Voluptas sit aspernatur te natus accusan maiores alias consequatur aut equatur aut perferendi.
    </p>
  </div>
  <div class="services__container">
    {#each services as service}
    <div class="services__container__item">
      <img class="services__icon" src="{service.img}" alt="" />
      <h3>{service.name}</h3>
      <p>{service.p}</p>
    </div>
    {/each}
  </div>
</section>
