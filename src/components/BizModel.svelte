<script>
  export let title;
  export let items;
  export let image;
</script>

<div class="biz-model-block" id="business">
  <div class="container">
    <div class="biz-model-content">
      <h2>{title}</h2>
      {#each items as item}
        <div>
          <h3>{item.title}</h3>
          <p>{item.text}</p>
        </div>
      {/each}
    </div>

    <div class="biz-model-image">
      <img src={image} alt="AzureHill Holdings Business Model" loading="lazy" />
    </div>
  </div>
</div>

<style>
  .biz-model-block {
    width: 100%;
  }
  .container {
    width: 100%;
    max-width: 1024px;
    margin: 0 auto;
    padding: 2rem;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
  }

  .biz-model-content {
    width: 100%;
    padding: 2rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .biz-model-image {
    width: 100%;
    padding: 2rem;
  }
</style>
