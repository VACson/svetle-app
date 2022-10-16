<script>
  import FacebookIcon from '../assets/icons/Facebook.svelte';
  import TwitterIcon from '../assets/icons/Twitter.svelte';
  import LinkedinIcon from '../assets/icons/Linkedin.svelte';
  import BallIcon from '../assets/icons/Ball.svelte';
  import YoutubeIcon from '../assets/icons/Youtube.svelte';
  import { links } from './links.js';

  const socials = [
    { href: 'https://uk-ua.facebook.com/', Icon: FacebookIcon },
    { href: 'https://twitter.com/home', Icon: TwitterIcon },
    { href: 'https://www.linkedin.com/', Icon: LinkedinIcon },
    { href: 'https://uk-ua.facebook.com/', Icon: BallIcon },
    { href: 'https://www.youtube.com/', Icon: YoutubeIcon },
  ];
  const iconColor = '#9FAAAB';
  let value = '';
  const placeholder = 'Write Your Email Address';

  function handleSubmit(e) {
    const formData = new FormData(e.target);
    const data = {};
    for (const [key, value] of formData) {
      data[key] = value;
    }
    value = '';
    const message = 'Thank you for subscription ' + data.email;
    console.log(data);
    alert(message);
  }
</script>

<footer class="footer">
  <div class="footer__details">
    <div class="header__logo footer__logo">
      <div class="header__logo__text">Portfo.</div>
      <div class="header__logo__circle" />
    </div>
    <form class="footer__details__form" on:submit|preventDefault={handleSubmit} action="">
      <p>Subscribe to newsletter to get some updates related with branding, designs and more.</p>
      <input id="email" name="email" type="email" bind:value {placeholder} />
      <button class="button button__footer" type="submit">SUBSCRIBE</button>
    </form>
    <div class="footer__details__links">
      {#each links as link}
        <a class="footer__details__links__item" href={link.href}>{link.label}</a>
      {/each}
    </div>
    <div class="footer__details__sidetext">
      <p>
        Just feel free to contact if you wanna collaborate with me, or simply have a conversation.
      </p>
      <a class="footer__details__sidetext__email" href="mailto:webmaster@somedomain.com"
        >templatesjungle@gmail.com</a
      >
    </div>
  </div>
  <div class="footer__bottom">
    <div class="footer__bottom__social">
      {#each socials as social}
        <a href="https://uk-ua.facebook.com/" target="_blank"
          ><svelte:component this={social.Icon} /></a
        >
      {/each}
    </div>
    <span class="footer__bottom__author">©2022, Portfo by <u>TemplatesJungle.</u></span>
  </div>
</footer>

<style>
  input {
    width: 100%;
    height: 56px;
    background: #f4f4f0;
    border: 1px solid #111111;
    border-radius: 8px;
    gap: 10px;
    padding: 12px 20px;
    color: #303030;
    font-size: 18px;
    margin-top: 20px;
    margin-bottom: 15px;
  }
</style>
