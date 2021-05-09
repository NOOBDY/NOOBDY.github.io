<script>
  import ProjectTemplate from "./ProjectTemplate.svelte";
  import projects from "./projects.json";
</script>

<div class={$$props.class} id="projects">
  <div class="wrapper">
    <h1 style="font-size: 6vmin;">projects</h1>
    {#each projects as project}
      <ProjectTemplate {project} />
    {/each}
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
