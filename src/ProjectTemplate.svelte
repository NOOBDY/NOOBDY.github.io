<script>
    import Projects from "./Projects.svelte";
</script>

<div class="project">
    <a href={$$props.github_src}>
        <img src={$$props.img_src} alt="" />
    </a>
    <h1>{$$props.title}</h1>
    <p>{$$props.p}</p>
</div>

<style>
    .project {
        text-align: center;
    }
    img {
        height: 10rem;
        width: 10rem;
        object-fit: contain;
    }
</style>
