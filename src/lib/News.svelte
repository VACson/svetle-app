<script>
  import coffee from '../assets/gallery/coffee.png';
  import painting from '../assets/gallery/painting.png';
  import window from '../assets/gallery/window.png';

  import { compareAsc, format } from 'date-fns';

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
      date: format(new Date(2022, 8, 12), 'MMM dd, yyyy'),
      heading: 'Graphic Designing Useful Tips & Best Practices',
    },
    {
      image: window,
      category: 'Branding',
      date: format(new Date(2022, 8, 12), 'MMM dd, yyyy'),
      heading: 'Best way to do branding of digital products ',
    },
    {
      image: painting,
      category: 'Branding',
      date: format(new Date(2022, 8, 12), 'MMM dd, yyyy'),
      heading: 'Top 10 graphic designs review in 2022 ',
    },
  ];
</script>

<section class="news">
  <h2 class="heading-2 font-inter">Latest News</h2>
  <p class="paragraph">Accusan maiores alias conseaut equatur aut perferendi.</p>
  <div class="news__article">
    {#each newsData as news}
      <a href="#" class="news__article__info">
        <img src={news.image} class="news__article__image" alt="" />
        <div class="news__article__info__details font-work-sans">
          <div class="news__article__info__details__date font-work-sans">
            <span class="span">{news.category}</span><span class="span">&#160;&#160;/&#160;</span>
            <span class="span">{news.date}</span>
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
