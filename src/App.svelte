<script>
  import WIP from "./WIP.svelte";
  import Home from "./Home.svelte";
  import NavBar from "./NavBar.svelte";
  import About from "./About.svelte";
</script>

<main class="container">
  <!--
  <WIP />
  -->
  <NavBar />
  <Home class="section" />
  <About class="section" />
</main>

<style>
  main {
    scrollbar-width: none;
    scroll-behavior: smooth;
    font-family: "Poppins", sans-serif;
  }
  .container {
    position: relative;
    width: 100%;
    height: 100vh;
    overflow: auto;
    scroll-snap-type: y mandatory;
  }
  .container :global(.section) {
    position: relative;
    width: 100%;
    height: 100vh;
    scroll-snap-align: start;
  }
</style>
