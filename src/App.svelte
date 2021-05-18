<script>
  import { Router, Link, Route } from "svelte-routing";
  import Home from "./routes/Home.svelte";
  import Music from "./routes/Music.svelte";
  import Dumpcast from "./routes/Dumpcast.svelte";
  import Shop from "./routes/Shop.svelte";

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
      <Link to="/shop" onmousedown="party.confetti(this)"
      ><div class="routelink">Shop</div></Link>
      <!-- svelte-ignore a11y-missing-attribute -->
      <a><div class="routelink" on:click={scrollToBottom}>Social Media</div></a>
    </nav>
  </header>
  <div>
    <Route path="/" component={Home} />
    <Route path="/music" component={Music} />
    <Route path="/dumpcast" component={Dumpcast} />
    <Route path="/shop" component={Shop} />
  </div>
</Router>

<Footer />

<style>
  #dumpster-header {
    font-size: 10vw;
  }

  @media screen and (max-aspect-ratio: 1/1) {
    nav {
    display:flex;
    justify-content: center; 
    flex-direction: column;
  }
  
  }

  
  
</style>
