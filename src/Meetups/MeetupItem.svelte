<script>
  import Button from '../UI/Button.svelte';

  export let id = '';
  export let title = '';
  export let subtitle = '';
  export let imageUrl = '';
  export let description = '';
  export let address = '';
  export let contactEmail = '';
</script>

<article>
  <header>
    <h1 class="">{title}</h1>
    <h2>{subtitle}</h2>
    <p>{address}</p>
  </header>
  <div>
    <img src={imageUrl} class="image" />
  </div>
  <div class="content">
    <p>{description}</p>
  </div>
  <footer>
    <Button href={contactEmail} caption="Contact" />
    <Button type="button" caption="Show Details" />
    <Button type="button" caption="Favorite" mode="outline" />
  </footer>
</article>

<style>
  article {
    /* position: relative;
    top: 5rem;
    overflow: hidden;
    z-index: -1; */
    position: relative;
    top: 4rem;
    display: flex;
    flex-direction: column;
    align-items: left;
    border: 1px solid #ccc;
    margin: 10px;
    padding: 15px;
    box-shadow: 1px 1px 7px rgba(88, 86, 86, 0.26);
  }

  h2 {
    font-size: 20px;
  }
</style>
