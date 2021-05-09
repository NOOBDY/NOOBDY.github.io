<script>
  import ProjectTemplate from "./ProjectTemplate.svelte";
  import * as DiscordBot from "./Projects/DiscordBot.json";
</script>

<div class={$$props.class} id="projects">
  <h1 class="title">projects</h1>
  <div>
    <ProjectTemplate
      title={DiscordBot.title}
      p={DiscordBot.description}
      img_src={DiscordBot.img_src}
      github_src={DiscordBot.github}
    />
  </div>
</div>

<style>
  .title {
    position: absolute;
    font-size: 6vmin;
    margin-right: 50vw;
    margin-bottom: 70vh;
  }
</style>
