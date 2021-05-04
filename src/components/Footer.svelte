<script>
function repion() {
  let ionicons = document.querySelectorAll('ion-icon');
  ionicons.forEach(icon => {
    let properTitle = icon.getAttribute('title');
    if (properTitle) {
      icon.shadowRoot.querySelector('.icon-inner svg title').innerHTML = properTitle
    }
  });
}
</script>

<footer>
  <ul class="social-media-list">
    <li>
      <a
        href="https://www.instagram.com/dumpsterfiremusic"
        class="logo-instagram"
        title="Instagram"
      >
        <ion-icon name="logo-instagram" title="Instagram"/>
      </a>
    </li>
    <li>
      <a
        href="https://www.youtube.com/channel/UCUvO8Nw5ijE2XVi110XOw7Q"
        class="logo-youtube"
        title="YouTube"
      >
        <ion-icon name="logo-youtube" />
      </a>
    </li>
    <li>
      <a
        href="https://discord.gg/A5sdKJt6Ah"
        class="logo-discord"
        title="Discord"
      >
        <ion-icon name="logo-discord" />
      </a>
    </li>
    <li>
      <a
        href="https://twitter.com/dumpfiremusic"
        class="logo-twitter"
        title="Twitter"
      >
        <ion-icon name="logo-twitter" />
      </a>
    </li>
    <li>
      <a
        href="https://www.tiktok.com/@dumpsterfiremusic"
        class="logo-tiktok"
        title="TikTok"
      >
        <ion-icon name="logo-tiktok" />
      </a>
    </li>
    <li>
      <a
        href="https://snapchat.com/add/dumpfiremusic"
        class="logo-snap"
        title="Snapchat"
      >
        <ion-icon name="logo-snapchat" />
      </a>
    </li>
    <li>
      <a
        href="https://www.reddit.com/r/dumpsterfiremusic"
        class="logo-reddit"
        title="Reddit"
      >
        <ion-icon name="logo-reddit" />
      </a>
    </li>
    <li>
      <a
        href="https://twitch.tv/dumpsterfirestreams"
        class="logo-twitch"
        title="Twitch"
      >
        <ion-icon name="logo-twitch" />
      </a>
    </li>
    <li>
      <a href="https://honk.me/dumpsterfire" class="logo-honk" title="Logo Honk">
        <ion-icon src="images/honk.svg" />
      </a>
    </li>
  </ul>
  Dumpster Fire © 2021
</footer>

<style>
  .social-media-list {
    list-style: none;
  }

  .social-media-list li {
    display: inline-block;
    margin-right: 1em;
    font-size: 180%;
  }

  .social-media-list li a {
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
    color: #7289da;
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

  /* ion-icon {
    pointer-events: none;
  } */
</style>
