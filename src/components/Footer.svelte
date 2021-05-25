<script>
  function repion() {
    let ionicons = document.querySelectorAll("ion-icon");
    ionicons.forEach((icon) => {
      let properTitle = icon.getAttribute("title");
      if (properTitle) {
        icon.shadowRoot.querySelector(".icon-inner svg title").innerHTML =
          properTitle;
      }
    });
  }


  let promo;

  fetch("https://api.dumpster.fr/shop/promo")
    .then(res => {
      res.json()
        .then(j => promo = j)
        .catch(err => console.error(err));
    })
    .catch(err => console.error(err));
</script>

<footer>
  <div class="container">
    <a
      target="_blank"
      href="https://link.dumpster.fr/instagram"
      class="logo-instagram"
      title="Instagram"
    >
      <ion-icon size="large" name="logo-instagram" title="Instagram" />
    </a>

    <a
      target="_blank"
      href="https://link.dumpster.fr/youtube"
      class="logo-youtube"
      title="YouTube"
    >
      <ion-icon size="large" name="logo-youtube" />
    </a>

    <a
      target="_blank"
      href="https://link.dumpster.fr/discord"
      class="logo-discord"
      title="Discord"
    >
      <ion-icon size="large" src="images/discord.svg" />
    </a>

    <a
      target="_blank"
      href="https://link.dumpster.fr/twitter"
      class="logo-twitter"
      title="Twitter"
    >
      <ion-icon size="large" name="logo-twitter" />
    </a>

    <a
      target="_blank"
      href="https://link.dumpster.fr/tiktok"
      class="logo-tiktok"
      title="TikTok"
    >
      <ion-icon size="large" name="logo-tiktok" />
    </a>

    <a
      target="_blank"
      href="https://link.dumpster.fr/snapchat"
      class="logo-snap"
      title="Snapchat"
    >
      <ion-icon size="large" name="logo-snapchat" />
    </a>

    <a
      target="_blank"
      href="https://link.dumpster.fr/reddit"
      class="logo-reddit"
      title="Reddit"
    >
      <ion-icon size="large" name="logo-reddit" />
    </a>

    <a
      target="_blank"
      href="https://link.dumpster.fr/twitch"
      class="logo-twitch"
      title="Twitch"
    >
      <ion-icon size="large" name="logo-twitch" />
    </a>

    <a
      target="_blank"
      href="https://link.dumpster.fr/honk"
      class="logo-honk"
      title="Logo Honk"
    >
      <ion-icon src="images/honk.svg" size="large" />
    </a>

    <a
      target="blank"
      class="logo-soundcloud"
      href="https://link.dumpster.fr/soundcloud"
      ><ion-icon name="logo-soundcloud" size="large" /></a
    >

    <a href="mailto:spencersolberg@dumpster.fr" class="logo-mail">
      <ion-icon size="large" name="mail-outline" />
    </a>
  </div>
  {#if promo}
  <nav id="promo-nav">
  <a id="promo-button" href={"https://shop.dumpster.fr/&couponCode=" + promo.code}>{promo.description}!</a>
  
</nav>
  
  {/if}

  Dumpster Fire © 2021
</footer>

<style>
  .container a {
    color: #888;
    transition: color 0.5s;
  }

  .logo-instagram:hover {
    color: #e1306c;
  }

  .logo-youtube:hover {
    color: #ff0000;
  }

  .logo-discord:hover {
    color: #5865f2;
  }

  .logo-twitter:hover {
    color: #1da1f2;
  }

  .logo-tiktok:hover {
    color: #ff0050;
  }

  .logo-snap:hover {
    color: #fffc00;
  }

  .logo-twitch:hover {
    color: #6441a5;
  }

  .logo-reddit:hover {
    color: #ff5700;
  }

  .logo-honk:hover {
    color: #018dff;
  }

  .logo-soundcloud:hover {
    color: #FF7F34;
  }

  .logo-mail:hover {
    color: #ead8b7;
  }

  .container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }

  .container ul {
    padding: 0;
  }

  .container a {
    padding: 1em;
  }

  #promo-nav {
    padding-top: 0;
  }
  #promo-button {
    background-color: rgb(255, 165, 0);
    color: white !important;
  }

</style>
