<script>
  export let item;
  export let onClick;
</script>

<li class="nav-item">
  <a class="nav-link raleway-700 {item.classes}" href="#" on:click={onClick}>
    {item.text}
  </a>
</li>

<style>
  .nav-link {
    text-transform: uppercase;
    text-decoration: none;
    color: #0f1728;
  }
</style>
