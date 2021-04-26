<script>
    const project = $$props.project;
</script>

<div class="project">
    <a href={project.github_src}>
        <img src={project.img_src} alt="" />
    </a>
    <h1>{project.title}</h1>
    <p>{project.description}</p>
</div>

<style>
    .project {
        text-align: center;
        margin: 1rem;
        width: 20vmax;
        max-width: 250px;
    }
    img {
        height: 10vmax;
        width: 10vmax;
        object-fit: contain;
        transition: 200ms;
    }
    img:hover {
        transform: scale(150%);
    }
    .project h1 {
        font-size: 4vmin;
    }
    .project p {
        font-size: 1rem;
    }
</style>
