<script>
  import { scrollToEl } from "./functions";
</script>

<nav id="nav">
  <ul>
    <li on:click={() => scrollToEl("home")}>home</li>
    <li on:click={() => scrollToEl("about")}>about</li>
    <li on:click={() => scrollToEl("projects")}>projects</li>
  </ul>
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
  #nav ul {
    text-align: center;
    padding: 0;
    transform: translateX(20%);
    list-style-type: none;
  }
  li {
    display: inline;
    color: #000000;
    font-size: 1.6vmax;
    margin: auto 5px;
    cursor: pointer;
  }
</style>
