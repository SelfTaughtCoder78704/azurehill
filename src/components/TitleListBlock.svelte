<script>
  export let title;
  export let items;
</script>

<div class="title-list-block" id="about">
  <div class="container">
    <h2>{title}</h2>
    <div class="title-list">
      {#each items as item}
        <p>{@html item}</p>
      {/each}
    </div>
  </div>
</div>

<style>
  .title-list-block {
    width: 100%;
  }

  .container {
    width: 100%;
    max-width: 1024px;
    margin: 0 auto;
    padding: 2rem;
    background: linear-gradient(
      180deg,
      #aadcfe 0%,
      rgba(170, 220, 254, 0) 100%
    );
  }

  h2 {
    text-align: center;
  }

  .title-list {
    display: flex;
    flex-direction: column;
  }
</style>
