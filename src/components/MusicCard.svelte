<script>
    export let album;
</script>

<article class="release">
    
    <div class="info">
        <h2 class="title"><a href={album.url}>{album.title}</a> <ion-icon
            class="share-button"
            name="share-outline"
            size="large"
            on:click={() => {
              navigator.share({
                title: album.title + " - Dumpster Fire",
                url: album.url,
              });
            }}
          /></h2>
          <div class="artwork">
            <a href={album.url}><img src={album.artwork.src} alt={album.artwork.alt} /></a>
        </div>
        {#each album.paragraphs as paragraph}
            <p class="paragraph">{paragraph}</p>
        {/each}
        
    </div>
    <nav><a href={album.url}><i class="fas fa-headphones"></i> Listen now</a></nav>
</article>

<style>
    .release,
    .artwork {
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        justify-content: space-between;
    }
    .artwork {
        flex: 3 1 30ch;
    }
    .release {
        background: linear-gradient(238.72deg, #FFE5C7 0%, #00C288 100%), radial-gradient(90.88% 100% at 50% 0%, #439246 0%, #183766 100%), linear-gradient(121.28deg, #FFEAB6 0%, #003C2A 100%), radial-gradient(64.89% 100% at 50% 0%, #80BAFF 0%, #001E41 100%), linear-gradient(65.05deg, #6F0072 0%, #FFC700 100%);
background-blend-mode: overlay, screen, color-burn, lighten, normal;
        border-radius: 5px;
    }
    .artwork,
    .info {
        padding: 5%;
    }

    .info h2 {
        margin-top: 0;
        margin-bottom: 0;
    }

    .paragraph {
        color: rgb(220, 220, 220);
    }
    .share-button {
        color: rgb(33, 33, 33);
    }
    .title a {
        text-decoration: none;
    }
</style>
