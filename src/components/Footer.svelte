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
</script>

<footer>
  <div class="container">
    <a
      target="_blank"
      href="https://www.instagram.com/dumpsterfiremusic"
      class="logo-instagram"
      title="Instagram"
    >
      <ion-icon size="large" name="logo-instagram" title="Instagram" />
    </a>

    <a
      target="_blank"
      href="https://www.youtube.com/channel/UCUvO8Nw5ijE2XVi110XOw7Q"
      class="logo-youtube"
      title="YouTube"
    >
      <ion-icon size="large" name="logo-youtube" />
    </a>

    <a
      target="_blank"
      href="https://discord.gg/A5sdKJt6Ah"
      class="logo-discord"
      title="Discord"
    >
      <ion-icon size="large" src="images/discord.svg" />
    </a>

    <a
      target="_blank"
      href="https://twitter.com/dumpfiremusic"
      class="logo-twitter"
      title="Twitter"
    >
      <ion-icon size="large" name="logo-twitter" />
    </a>

    <a
      target="_blank"
      href="https://www.tiktok.com/@dumpsterfiremusic"
      class="logo-tiktok"
      title="TikTok"
    >
      <ion-icon size="large" name="logo-tiktok" />
    </a>

    <a
      target="_blank"
      href="https://snapchat.com/add/dumpfiremusic"
      class="logo-snap"
      title="Snapchat"
    >
      <ion-icon size="large" name="logo-snapchat" />
    </a>

    <a
      target="_blank"
      href="https://www.reddit.com/r/dumpsterfiremusic"
      class="logo-reddit"
      title="Reddit"
    >
      <ion-icon size="large" name="logo-reddit" />
    </a>

    <a
      target="_blank"
      href="https://twitch.tv/dumpsterfirestreams"
      class="logo-twitch"
      title="Twitch"
    >
      <ion-icon size="large" name="logo-twitch" />
    </a>

    <a
      target="_blank"
      href="https://honk.me/dumpsterfire"
      class="logo-honk"
      title="Logo Honk"
    >
      <ion-icon src="images/honk.svg" size="large" />
    </a>

    <a
      target="blank"
      class="logo-soundcloud"
      href="https://soundcloud.com/user-736900638"
      ><ion-icon name="logo-soundcloud" size="large" /></a
    >

    <a href="mailto:spencersolberg@dumpster.fr" class="logo-mail">
      <ion-icon size="large" name="mail-outline" />
    </a>
  </div>
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
</style>
