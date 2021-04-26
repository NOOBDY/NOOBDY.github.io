<script>
  import ProjectTemplate from "./ProjectTemplate.svelte";
  import DiscordBot from "./Projects/DiscordBot";
</script>

<div class={$$props.class} id="projects">
  <h1 class="title">projects</h1>
  <div id="project-list">
    <ProjectTemplate project={DiscordBot} />
  </div>
</div>

<style>
  .title {
    position: absolute;
    font-size: 6vmin;
    margin-right: 50vw;
    margin-bottom: 70vh;
  }
  #project-list {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
  }
</style>
