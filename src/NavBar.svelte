<script>
  function scrollToEl(id) {
    var element = document.getElementById(id);
    element.scrollIntoView();
  }
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
    position: fixed;
    margin: 0;
    padding: 0;
    z-index: 1;
    width: 100%;
    height: 3rem;
  }
  #nav ul {
    list-style-type: none;
    position: absolute;
    top: 50%;
    left: 70%;
    transform: translate(-50%, -50%);
  }
  li {
    display: inline;
    color: #000000;
    font-size: 20px;
    margin: auto 5px;
    cursor: pointer;
  }
</style>
