<h2>Coming soon! <ion-icon class="share-button" name="share-outline" size="large" on:click={() => {
    navigator.share({
      title: "Dumpster Fire - Music",
      url: location.href
    });
  }}/></h2>
