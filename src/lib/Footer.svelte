<script>
  import { links } from './links.js';
  import { socials } from './socialsInFooter.js';

  let value = '';

  function handleSubmit(e) {
    const formData = new FormData(e.target);
    const data = {};
    for (const [key, value] of formData) {
      data[key] = value;
    }
    value = '';
    const message = 'Thank you for subscription ' + data.email;
    data.email !== '' && alert(message);
  }
</script>

<footer class="footer">
  <div class="footer__details">
    <div class="header__logo footer__logo">
      <div class="header__logo__text">Portfo.</div>
      <div class="header__logo__circle" />
    </div>
    <form class="footer__details__form" on:submit|preventDefault={handleSubmit} action="">
      <p class="paragraph">
        Subscribe to newsletter to get some updates related with branding, designs and more.
      </p>
      <input
        class="input"
        id="email"
        name="email"
        type="email"
        bind:value
        placeholder="Write Your Email Address"
      />
      <button class="button button__footer" type="submit" tabindex="0">SUBSCRIBE</button>
    </form>
    <div class="footer__details__links">
      {#each links as link, i}
        <a class="footer__details__links__item" href={link.href} tabindex={i}>{link.label}</a>
      {/each}
    </div>
    <div class="footer__details__sidetext">
      <p class="paragraph">
        Just feel free to contact if you wanna collaborate with me, or simply have a conversation.
      </p>
      <a class="footer__details__sidetext__email" href="mailto:templatesjungle@gmail.com"
        >templatesjungle@gmail.com</a
      >
    </div>
  </div>
  <div class="footer__bottom">
    <div class="footer__bottom__social">
      {#each socials as social, i}
        <a class="footer__bottom__social__icon" href={social.href} target="_blank" tabindex={i}
          ><svelte:component this={social.Icon} /></a
        >
      {/each}
    </div>
    <span class="footer__bottom__author">©2022, Portfo by <u>TemplatesJungle.</u></span>
  </div>
</footer>

<style>
  .input {
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
    transition: 0.3s;
  }
  .input:focus {
    transition: 0.3s;
    padding: 14px 22px;
    border: 4px solid #4ba1a7;
  }
</style>
