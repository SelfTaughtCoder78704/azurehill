<script>
  export let items = [];
  export let logo = "/logo.svg";

  export let handleClick = (event) => {
    const active = document.querySelector(".active");

    active.classList.remove("active");
    event.target.classList.add("active");
  };
</script>

<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" href="/">
    <img src={logo} alt="AzureHill Holdings Logo" loading="lazy" />
  </a>
  <ul class="navbar-nav">
    {#each items as item}
      <li class="nav-item">
        <a
          class="nav-link raleway-700 {item.classes}"
          href="#{item.section}"
          on:click={handleClick}
        >
          {item.text}
        </a>
      </li>
    {/each}
  </ul>
</nav>

<style>
  .navbar {
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
    background-color: #aadcfe;
    padding: 0.5rem 100px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }

  .navbar-brand {
    display: block;
    width: 100%;
  }

  .navbar-brand img {
    display: block;
    width: 70px;
  }

  .navbar-nav {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 100%;
    list-style: none;
  }

  .nav-link {
    text-transform: uppercase;
    text-decoration: none;
    color: #0f1728;
  }
</style>
