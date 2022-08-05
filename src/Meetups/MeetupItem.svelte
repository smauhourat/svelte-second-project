<script>
  export let title = "";
  export let subtitle = "";
  export let image = "";
  export let content = "";
</script>

<article>
  <header>
    <h1 class="">{title}</h1>
    <h2>{subtitle}</h2>
  </header>
  <div>
    <img src={image} class="image" />
  </div>
  <div class="content">
    <p>Content</p>
  </div>
  <footer>
    <button>Show Details</button>
    <button>Favorite</button>
  </footer>
</article>

<style>
  article {
    position: relative;
    top: 5rem;
    overflow: hidden;
    z-index: -1;
    display: flex;
    flex-direction: column;
    align-items: left;
    border: 1px solid #ccc;
    margin: 10px;
    padding: 15px;
    box-shadow: 1px 1px 7px rgba(88, 86, 86, 0.26);
  }
</style>
