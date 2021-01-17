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
  .container {
    position: relative;
    width: 100%;
    height: 100vh;
  }
  .container :global(.section) {
    width: 100%;
    height: 100vh;
  }
</style>
