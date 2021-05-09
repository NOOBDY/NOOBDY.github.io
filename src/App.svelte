<script>
  import WIP from "./WIP.svelte";
  import Home from "./Home.svelte";
  import NavBar from "./NavBar.svelte";
  import About from "./About.svelte";
  import Projects from "./Projects.svelte";

  let shown = false;
</script>

<main class="container">
  <WIP class="section" bind:shown />
  {#if shown}
    <NavBar />
    <Home class="section" />
    <About class="section" />
    <Projects class="section" />
  {/if}
</main>

<style>
  main {
    scrollbar-width: none;
    scroll-behavior: smooth;
    font-family: "Poppins", sans-serif;
  }
  main::-webkit-scrollbar {
    display: none;
  }
  .container {
    position: relative;
    width: 100%;
    height: 100vh;
    overflow: auto;
    scroll-snap-type: y mandatory;
  }
  .container :global(.section) {
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    width: 100%;
    height: 100vh;
    scroll-snap-align: start;
  }
</style>
