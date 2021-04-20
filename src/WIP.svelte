<script>
  import { createEventDispatcher } from "svelte";

  export let shown = false;

  let dispatch = createEventDispatcher();

  function show() {
    shown = !shown;
    dispatch("show", shown);
  }
</script>

<div class={$$props.class} id="wip">
  <div id="description">
    <h1>Hi! This is my GitHub Page</h1>
    <h2>This site is still under development</h2>
    <p>
      View my profile and other projects
      <a href="https://github.com/NOOBDY">here</a>
    </p>
  </div>
  <div id="bg-text">
    <p on:click={show}>work in progress...</p>
  </div>
</div>

<style>
  #description {
    text-align: center;
  }
  #description h1 {
    font-size: 5vmin;
  }
  #description h2 {
    font-size: 4vmin;
  }
  #description p {
    font-size: 3vmin;
  }
  #bg-text {
    display: flex;
    justify-content: center;
    align-items: center;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
  }
  #bg-text p {
    font-size: 5vw;
    font-family: "PT Mono", monospace;
    white-space: nowrap;
    color: #b6b6b6;
    margin-left: 2.5rem;
  }
</style>
