<script lang="ts">
  import { scrollToEl } from "./functions";

  let navBarItems = ["home", "about", "projects"];
</script>

<nav id="nav">
  <div id="items">
    {#each navBarItems as item}
      <p class="item" on:click={() => scrollToEl(item)}>{item}</p>
    {/each}
  </div>
</nav>

<style>
  #nav {
    display: block;
    position: sticky;
    top: 2vh;
    margin: 0;
    padding: 0;
    z-index: 1;
    height: 3rem;
  }
  #items {
    display: flex;
    justify-content: center;
    text-align: center;
    padding: 0;
    transform: translateX(20%);
    list-style-type: none;
  }
  .item {
    color: #000000;
    font-size: 1.6vmax;
    margin: auto 5px;
    cursor: pointer;
  }
</style>
