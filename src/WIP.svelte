<script>
  import { createEventDispatcher } from "svelte";
  import { scrollToEl } from "./functions";

  export let shown = false;

  let dispatch = createEventDispatcher();
  let counter = 0;

  console.log("click around to discover something!");

  function show() {
    counter++;
    if (counter === 3) {
      shown = true;
      dispatch("show", shown);

      setTimeout(() => {
        scrollToEl("home");
      }, 200);
    }
  }
</script>

<div class={$$props.class} id="wip">
  <div id="description">
    <h1 style="font-size: 5vmin">Hi! This is my GitHub Page</h1>
    <h2 style="font-size: 4vmin;">This site is still under development</h2>
    <p style="font-size: 3vmin;">
      View my profile and other projects
      <a href="https://github.com/NOOBDY">here</a>
    </p>
  </div>
  <div id="bg-text">
    <p on:click={show}>
      work in progress{#if counter >= 1}.{/if}{#if counter >= 2}.{/if}{#if counter >= 3}.{/if}
    </p>
  </div>
</div>

<style>
  #description {
    position: absolute;
    margin-bottom: 60vh;
    text-align: center;
  }
  #bg-text {
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
  }
  #bg-text p {
    font-size: 6vw;
    font-family: "PT Mono", monospace;
    white-space: nowrap;
    color: #b6b6b6;
  }
</style>
