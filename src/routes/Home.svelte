<script>
  import MaskRaffle from "../components/embeds/MaskRaffle.svelte";
  import { Link } from "svelte-routing";
</script>

<main>
  <h2>Here's the situation!</h2>
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
  <ul>
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
  <MaskRaffle />
</main>

<style>
  .dumpsterfire3 {
    aspect-ratio: 1/1;
  }
  .dumpsterfirewithjustin {
    aspect-ratio: 1080/898;
  }
</style>
