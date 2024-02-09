<script>
  export let image;
  export let content;
  export let hasH1 = false;
</script>

<div class="callout" id="home">
  <div class="container">
    <div class="callout-image">
      <img src={image} alt={content.title} loading="lazy" />
    </div>
    <div class="callout-content">
      {#if hasH1}
        <h1>{content.title}</h1>
      {:else}
        <h2>{content.title}</h2>
      {/if}
      <p>{content.description}</p>
    </div>
  </div>
</div>

<style>
  .callout {
    width: 100%;
    padding-top: 150px;
  }

  .container {
    width: 100%;
    max-width: 1024px;
    margin: 0 auto;
    display: flex;
    flex-direction: row-reverse;
    align-items: center;
    justify-content: center;
  }

  .callout-image {
    width: 50%;
    padding: 2rem;
  }

  .callout-image img {
    width: 100%;
    height: 100%;
  }

  .callout-content {
    width: 50%;
    padding: 2rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  h1 {
    margin-bottom: 10px;
  }
  p {
    margin-top: 0;
  }
</style>
