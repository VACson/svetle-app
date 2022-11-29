<script>
  import Background from '../assets/Bg.png';
  import BurgerIcon from '../assets/burgermenu.svelte';
  import ArrowIcon from '../assets/Arrow.svelte';
  import { links } from './links.js';
  import { socials } from './socials.js';

  let menu = { isOpen: false };

  function menuInteract() {
    menu.isOpen = !menu.isOpen;
  }
  function scroll() {
    window.scrollTo({
      top: 1000,
      behavior: 'smooth',
    });
  }
</script>

<header class="header">
  <img class="header__img" src={Background} alt="" />
  <div class="header__section">
    <nav class="nav">
      <div class="header__logo">
        <div class="header__logo__text font-inter">Portfo.</div>
        <div class="header__logo__circle" />
      </div>
      {#if menu.isOpen}
        <div class="nav__menu">
          {#each links as link}
            <a class="nav__menu__link" href={link.href} on:click={menuInteract}>{link.label}</a>
          {/each}
        </div>{/if}
      <div class="nav__burger {menu.isOpen && 'nav__burger--active'}" on:click={menuInteract}>
        <svelte:component this={BurgerIcon} />
      </div>
    </nav>
    <div class="header__content">
      <div class="header__content__section">
        <h1 class="heading-1 font-inter">Chris Lee <br /> Creative Design</h1>
        <p class="caption paragraph">
          Make designs specially illustrations, logos, UI/UX, apps & websites, social media,
          magazines & banners.
        </p>
        <a href="/"><button class="button">CONTACT US</button></a>
      </div>
      <div class="header__content__icons">
        {#each socials as social}<a class="icon" href={social.href} target="_blank">
            <svelte:component this={social.Icon} />
          </a>{/each}
      </div>
    </div>
  </div>
  <div class="header__arrow" on:click={scroll}><svelte:component this={ArrowIcon} /></div>
</header>

<style>
  @media (max-width: 1200px) {
    .header__section, .header__content {
       padding: 10px;
       justify-content: start;
    }
    .header__content__icons {
      display: none;
    }
    
    .header__content__section {
      width: 100%;
    }
    .header__content__section a {
      margin: 400px auto 0 auto;
    }
    .nav__menu {
      top: 20px;
      right: 10px;
      width: 96%;
      height: fit-content;
    }
    .nav__menu__link {
      font-size: 24px;
      height: 40px;
    }
    .heading-1 {
      font-size: 36px;
      line-height: 40px;
    }
  }
</style>
