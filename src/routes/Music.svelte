<script>
  import MusicCard from "../components/MusicCard.svelte";

  const reachingOut = {
    title: "REACHING OUT",
    artwork: {
      src: "images/REACHINGOUT.webp",
      alt: 'The cover artwork for "REACHING OUT"',
    },
    paragraphs: [
      '"REACHING OUT" is Dumpster Fire\'s debut single. This genre-defying track will reform how you percieve music. The release has been praised as one of the greatest releases of 2021, and its expected to net Dumpster Fire numerous presitious awards.',
      "The song prominently features the four members of Dumpster Fire, as well as friends and special guest stars.",
    ],
    url: "https://link.dumpster.fr/reachingout"
  };
</script>

<main>
  <!-- <h2>
    Coming soon! <ion-icon
      class="share-button"
      name="share-outline"
      size="large"
      on:click={() => {
        navigator.share({
          title: "Dumpster Fire - Music",
          url: location.href,
        });
      }}
    />
  </h2> -->
<br>
  <!-- <MusicCard album={reachingOut} /> -->

  <iframe width="100%" height="150" src="https://odesli.co/embed/?url=https%3A%2F%2Fsong.link%2Freachingout&theme=dark" frameborder="0" allowfullscreen sandbox="allow-same-origin allow-scripts allow-presentation allow-popups allow-popups-to-escape-sandbox" allow="clipboard-read; clipboard-write"></iframe>
</main>

<style>
  /* .flex-span {
    display:flex;
    flex-wrap: wrap;
  }
  .reaching-out-container {
    display: flex;
    flex-direction: column;
    border-radius: 5px;
    background-color: #b02a44;
    justify-content: space-around;
  } */

  /* .reaching-out-container h2 {
    color: rgb(220, 220, 220);
    margin-left: auto;
    margin-right: auto;
  }
  #artwork {
    width: 50%;
    border-radius: 5px;
  }
  .reaching-out-container * {
    padding-left: 5%;
    padding-right: 5%;
  } */
</style>
