<script>
  import MaskRaffle from "../components/embeds/MaskRaffle.svelte";
  import { Link } from "svelte-routing";

  let sellables;

  fetch("https://api.dumpster.fr/shop/sellables")
    .then(res => {
      res.json()
        .then(j => sellables = j)
        .catch(err => console.error(err));
    })
    .catch(err => console.error(err));

  // let randomProduct = sellables.sellables[Math.floor(Math.random() * sellables.sellables.length)];

  
</script>

<main>
  <h2>Here's the situation! <ion-icon class="share-button" name="share-outline" size="large" on:click={() => {
    navigator.share({
      title: "Dumpster Fire - Home",
      url: location.href
    });
  }} /></h2>
  <figure>
    <img
      class="dumpsterfirewithjustin"
      src="images/dumpsterfirewithjustin.webp"
      alt="The dumpster fire boys with Justin Crichfield"
      loading="lazy"
    />
    <figcaption>
      The Dumpster Fire boys with Justin Crichfield (middle).
    </figcaption>
  </figure>

  <p class="desc">
    Dumpster Fire is a four member band from Wisconsin. The group produces a
    wide array of content ranging from podcasts to music and everything in
    between. Thanks for reaching out!
  </p>
  <br />

  <p>
    Dumpster Fire was founded January, 2020. Since then, it has grown to become
    a well-established brand internationally. The current roster includes:
  </p>
  <ul spellcheck="false" contenteditable="true">
    <li>Samuel Schoonover</li>
    <li>Spencer Solberg</li>
    <li>Spencer Sveen</li>
    <li>River Rommel</li>
  </ul>
  <figure>
    <img
      class="dumpsterfire3"
      src="images/dumpsterfire3.webp"
      alt="Three of the Dumpster Fire boys sitting down."
      loading="lazy"
    />
    <figcaption>
      Three members of Dumpster Fire while they were on tour. Unfortunately,
      Spencer Sveen was hit by a bus and was not in this photo.
    </figcaption>
  </figure>
  <p>
    Some notable projects from Dumpster Fire include <Link to="/dumpcast"
      >Dumpcast</Link
    > and the Dumpster Fire Mask Raffle:
  </p>
  <div style="margin-left:auto;margin-right:auto">
  <MaskRaffle/>

  {#if sellables}
  <a href="https://shop.dumpster.fr" style="text-decoration:none"><h2>The Dumpster Fire Shop</h2></a>
  <figure><a href="https://shop.dumpster.fr"><div id="rpi-con">
  <img loading="lazy" id="random-product-img" src={sellables.sellables[Math.floor(Math.random() * sellables.sellables.length)].previewImage.url} alt="A random Dumpster Fire product" /></div></a>
  <figcaption>You can find this product and {sellables.count - 1} more at <a href="https://shop.dumpster.fr">shop.dumpster.fr</a>!</figcaption>
</figure>
<p>The official Dumpster Fire Shop is now open! Shop for hoodies, t-shirts, accessories, and more at <a href="https://shop.dumpster.fr">shop.dumpster.fr</a>!</p>
<p>All sales/orders are handled by Spreadshirt.</p>
<nav id="my-nav-2">
  <a id="shop-button-2" href="https://shop.dumpster.fr/"><i class="fas fa-shopping-bag"></i> Shop now!</a>
</nav>
  {/if}
</div>
</main>

<style>
  .dumpsterfire3 {
    aspect-ratio: 1/1;
  }
  .dumpsterfirewithjustin {
    aspect-ratio: 1080/898;
  }
#my-nav-2 {
  display: flex;
  justify-content: center;
}
  #shop-button-2 {
    background-color: rgb(255, 165, 0);
    color: white !important;
  }

  #rpi-con {
    display: flex;
    justify-content: center;
  }
</style>
