<script>
  import { Router, Link, Route } from "svelte-routing";
  import Home from "./routes/Home.svelte";
  import Music from "./routes/Music.svelte";
  import Dumpcast from "./routes/Dumpcast.svelte";
  //   import SocialMedia from "./routes/SocialMedia.svelte";

  import Footer from "./components/Footer.svelte";
  (function () {
    var ticker = document.createElement("script");
    ticker.async = true;
    ticker.src = "https://embed.twitcker.com/ticker/dumpfiremusic.js";
    (
      document.getElementsByTagName("head")[0] ||
      document.getElementsByTagName("body")[0]
    ).appendChild(ticker);
  })();

  const scrollToBottom = () => {
    window.scrollTo(0, document.body.scrollHeight);
  };
</script>

<Router>
  <header>
    <h1>
      <i class="fas fa-dumpster-fire" />
      Dumpster Fire
    </h1>
    <h5>Thanks for reaching out!</h5>

    <nav>
      <Link to="/" onmousedown="party.confetti(this)"
        ><div class="routelink">Home</div></Link
      >
      <Link to="/music" onmousedown="party.confetti(this)"
        ><div class="routelink">Music</div></Link
      >
      <Link to="/dumpcast" onmousedown="party.confetti(this)"
        ><div class="routelink">Dumpcast</div></Link
      >
      <Link
        ><div class="routelink" on:click={scrollToBottom}>
          Social Media
        </div></Link
      >
      <!-- <Link to="/socialmedia" onmousedown="party.confetti(this)"
        ><div class="routelink">Social Media</div></Link
      > -->
    </nav>
  </header>
  <div>
    <Route path="/" component={Home} />
    <Route path="/music" component={Music} />
    <Route path="/dumpcast" component={Dumpcast} />
    <!-- <Route path="/socialmedia" component={SocialMedia} /> -->
  </div>
</Router>

<Footer />

<style>
  /* h1 {
    font-family: "Rock Salt", cursive;
  } */
  #twitcker-bar div.box {
    background: color(#ffa500);
  }
</style>
