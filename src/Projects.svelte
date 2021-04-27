<script>
  import ProjectTemplate from "./ProjectTemplate.svelte";
  import DiscordBot from "./Projects/DiscordBot";
</script>

<div class={$$props.class} id="projects">
  <div class="wrapper">
    <h1 style="font-size: 6vmin;">projects</h1>
    <ProjectTemplate project={DiscordBot} />
    <ProjectTemplate project={DiscordBot} />
  </div>
</div>

<style>
  .wrapper {
    display: flex;
    flex-direction: column;
    margin-right: 50vw;
    margin-top: 10vh;
  }
</style>
