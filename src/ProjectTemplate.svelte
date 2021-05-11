<script>
    import { slide } from "svelte/transition";

    const project = $$props.project;
    let shown = false;
    let transformValue = "0%";

    function update() {
        shown = !shown;
        transformValue = shown ? "5%" : "0%";
    }

    $: cssVarStyles = `--transform-value:${transformValue};`;
</script>

<div class="project">
    <h1 on:click={update} style={cssVarStyles}>
        {project.title}
    </h1>
    {#if shown}
        <div transition:slide={{ duration: 200 }}>
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
        transition: 200ms;
        transform: translateX(var(--transform-value));
    }
    .project p {
        font-size: 1rem;
    }
</style>
