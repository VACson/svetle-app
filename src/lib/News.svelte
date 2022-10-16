<script>
  import coffee from '../assets/gallery/coffee.png';
  import painting from '../assets/gallery/painting.png';
  import window from '../assets/gallery/window.png';
  const newsData = [
    // {
    //   image: coffee,
    //   category: 'Design',
    //   date: format(new Date('12/09/2022'), 'MMMM, dd, yyyy'),
    //   heading: 'Graphic Designing Useful Tips & Best Practices',
    // },
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
  <h2 class="heading-2 font-inter">Latest News</h2>
  <p class="paragraph">Accusan maiores alias conseaut equatur aut perferendi.</p>
  <div class="news__article">
    {#each newsData as news}
      <a href="#" class="news__article__info">
        <img src={news.image} class="news__article__image" alt="" />
        <div class="news__article__info__details font-work-sans">
          <div class="news__article__info__details__date">
            <span class="span">{news.category}</span><span class="span">{separators[0]}</span>
            <span class="span">{news.date.month}</span>
            <span class="span">{news.date.day}</span><span class="span">{separators[1]}</span>
            <span class="span">{news.date.year}</span>
          </div>
          <h3 class="heading-3 font-inter news__article__info__details__heading">
            {news.heading}
          </h3>
        </div>
      </a>
    {/each}
  </div>
  <button class="button button--blog">VIEW ALL BLOGS</button>
</section>

<style>
  .span {
    font-family: inherit;
    color: inherit;
    color: #303030;
  }
  .button--blog {
    width: 284px;
  }
</style>
