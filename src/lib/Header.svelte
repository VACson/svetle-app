<script>
  import Background from '../assets/Bg.png';
  import Burger from '../assets/burgermenu.svg';
  import Facebook from '../assets/icons/Facebook.svelte';
  import Instagram from '../assets/icons/Instagram.svelte';
  import Be from '../assets/icons/Be.svelte';
  import Twitter from '../assets/icons/twitter.svelte';
  import Pinterest from '../assets/icons/pinterest.svelte';
</script>

<header class="header">
  <img class="header__img" src={Background} alt="" />
  <div class="header__section">
    <nav class="nav">
      <div class="header__logo">
        <div class="header__logo__text">Portfo.</div>
        <div class="header__logo__circle" />
      </div>
      <img class="nav__burger" src={Burger} alt="" />
    </nav>
    <div class="header__content">
      <div class="header__content__section">
        <h1 class="h1">Chris Lee Creative Design</h1>
        <p class="caption">
          Make designs specially illustrations, logos, UI/UX, apps & websites, social media,
          magazines & banners.
        </p>
        <a href="/"><button class="button">CONTACT US</button></a>
      </div>
      <div class="header__content__icons">
        <a href="https://uk-ua.facebook.com/" target="_blank">
          <Facebook hover="#000" />
        </a>
        <a href="https://www.instagram.com/" target="_blank"> <Instagram /></a>
        <a href="/"> <Be /></a>
        <a href="https://twitter.com/home" target="_blank"> <Twitter hover="#000" /></a>
        <a href="https://www.pinterest.co.uk/" target="_blank"> <Pinterest /></a>
      </div>
    </div>
  </div>
</header>

<style>
  a {
    width: 50px;
    height: 50px;
    background-color: #fff;
    padding: 15px;
    border-radius: 50%;
  }
</style>
