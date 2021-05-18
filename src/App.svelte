<script>
  import { Router, Link, Route } from "svelte-routing";
  import Home from "./routes/Home.svelte";
  import Music from "./routes/Music.svelte";
  import Dumpcast from "./routes/Dumpcast.svelte";
  import Shop from "./routes/Shop.svelte";

  import smoothscroll from 'smoothscroll-polyfill';
  smoothscroll.polyfill();

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
    window.scroll({ top: document.body.scrollHeight, left: 0, behavior: 'smooth' });
  };

  const scrollToTop = () => {
    if (window.outerWidth > window.outerHeight) return;
    document.querySelector(".top").scrollIntoView({behavior: "smooth"});
  }

  const animateCSS = (element, animation, prefix = 'animate__') => {
  // We create a Promise and return it
  new Promise((resolve, reject) => {
    const animationName = `${prefix}${animation}`;
    const node = document.querySelector(element);

    node.classList.add(`${prefix}animated`, animationName);

    // When the animation ends, we clean the classes and resolve the Promise
    function handleAnimationEnd(event) {
      event.stopPropagation();
      node.classList.remove(`${prefix}animated`, animationName);
      resolve('Animation ended');
    }

    node.addEventListener('animationend', handleAnimationEnd, {once: true});
  });
}
  const shake = (element) => {
    animateCSS(element, "tada");
     
      setTimeout(() => {
        shake(element);
      }, 8000);
    
  };

  window.onload = () => {
    shake("#shop-button");
  }
</script>

<Router>
  <header>
    <a href="/" style="text-decoration:none;"><h1>
      <i class="fas fa-dumpster-fire" />
      Dumpster Fire
    </h1>
  </a>
    <h5>Thanks for reaching out!</h5>

    <nav> 
      <Link to="/" on:click={scrollToTop} onmousedown="party.confetti(this)"
        ><div class="routelink"><i class="fas fa-home"></i> Home</div></Link
      >
      <Link to="/music" on:click={scrollToTop} onmousedown="party.confetti(this)"
        ><div class="routelink"><i class="fas fa-music"></i> Music</div></Link
      >
      <Link to="/dumpcast" on:click={scrollToTop} onmousedown="party.confetti(this)"
        ><div class="routelink"><i class="fas fa-microphone"></i> Dumpcast</div></Link
      >
      <!-- <Link to="/shop" onmousedown="party.confetti(this)"
      > -->
      <a id="shop-button" href="https://shop.dumpster.fr"><div class="routelink"><i class="fas fa-shopping-bag"></i> Shop</div></a>
    <!-- </Link> -->
      <!-- svelte-ignore a11y-missing-attribute -->
      <a><div class="routelink" on:click={scrollToBottom}><i class="fas fa-user-friends"></i> Social Media</div></a>
    </nav>
  </header>
  <div class="top"></div>
  <div>
    <Route path="/" component={Home} />
    <Route path="/music" component={Music} />
    <Route path="/dumpcast" component={Dumpcast} />
    <Route path="/shop" component={Shop} />
  </div>
</Router>
<div id="myShop"></div>
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
    
    header {
      text-align: left;
    }
  
  }

</style>
