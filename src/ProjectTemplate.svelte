<script>
    import { slide } from "svelte/transition";

    const project = $$props.project;
    let shown = false;
</script>

<div class="project">
    <h1 on:click={() => (shown = !shown)}>
        {project.title}
    </h1>
    {#if shown}
        <div transition:slide>
            <p>{project.description}</p>
            <a href={project.github}>view source</a>
        </div>
    {/if}
</div>

<style>
    .project {
        margin: 1rem;
        margin: 2vw 0;
    }
    .project h1 {
        font-size: 6vmin;
        cursor: pointer;
        margin: 0;
        transition: 150ms;
    }
    .project h1:hover {
        transform: translateX(5%);
    }
    .project p {
        font-size: 1rem;
    }
</style>
