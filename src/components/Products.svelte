<script>
  export let title;
  export let items;
</script>

<div class="product-block" id="products">
  <div class="container">
    <h2>{title}</h2>
    <div class="list">
      {#each items as item}
        <div>
          <h3>{item.title}</h3>
          <p>{item.text}</p>
        </div>
      {/each}
    </div>
  </div>
</div>

<style>
  .product-block {
    width: 100%;
  }
  .container {
    width: 100%;
    max-width: 1024px;
    margin: 0 auto;
    padding: 2rem;
  }

  h2 {
    text-align: center;
  }

  .list {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    text-align: center;
  }

  .list div {
    width: 100%;
  }
</style>
