<script>
  import coffee from '../assets/gallery/coffee.png';
  import painting from '../assets/gallery/painting.png';
  import window from '../assets/gallery/window.png';
  const gallery = [
    {
      image: coffee,
      category: 'Design',
      date: { month: 'Sept', day: 12, year: 2022 },
      heading: 'Graphic Designing Useful Tips & Best Practices',
    },
    {
      image: window,
      category: 'Branding',
      date: { month: 'Sept', day: 12, year: 2022 },
      heading: 'Best way to do branding of digital products ',
    },
    {
      image: painting,
      category: 'Branding',
      date: { month: 'Sept', day: 12, year: 2022 },
      heading: 'Top 10 graphic designs review in 2022 ',
    },
  ];
  const separators = [' / ', ','];
</script>
<section class="news">
  <h2>Latest News</h2>
  <p>Accusan maiores alias conseaut equatur aut perferendi.</p>
  <div class="news__gallery">
    {#each gallery as block}
    <div class="news__gallery__info">
      <img src="{block.image}" class="news__gallery__image" alt="" />
      <span class="news__gallery__info__details"
        ><span class="">{block.category}</span><span class="">{separators[0]}</span>
        <span class="">{block.date.month}</span>
        <span class="">{block.date.day}</span><span class="">{separators[1]}</span>
        <span class="">{block.date.year}</span>
      </span>
      <h3 class="news__gallery__info__details news__gallery__info__details__heading">
        {block.heading}
      </h3>
    </div>
    {/each}
  </div>
  <button class="button">VIEW ALL BLOGS</button>
</section>
<style>
  span {
    color: inherit;
  }
</style>
