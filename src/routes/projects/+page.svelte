<!-- this is the projects page which list my current projects and links to them -->
<!-- on the right side of the page there is the tile and a description of the projects -->
<!-- on the left there is a photo with the link underneath it -->

<script context="module" lang="ts">
    import Header from '../Header.svelte';
    //import projects from './projects';
    const projects = [
        {
            name: "Project 1",
            description: "Dumb thing.",
            image: "https://via.placeholder.com/400x300",
            url: "https://example.com/project1",
        },
        {
            name: "Change the World",
            description: "This one is gonnna be crazy wack.",
            image: "https://via.placeholder.com/400x300",
            url: "https://example.com/project2",
        },
        // Add more projects here
    ];
</script>

<Header />
<h1>Projects</h1>

<div class="project-list">
    {#each projects as project}
      <div class="project">
        <h2>{project.name}</h2>
        <p>{project.description}</p>
        <a href={project.url} target="_blank"><img src={project.image} alt={project.name} /></a>
      </div>
    {/each}
</div>

<!-- <div> -->
<!--     <h1>Projects</h1> -->
<!--     <div class="project-names"> -->
<!--         <h3>Lyr</h3> -->
<!--         <h3>Yuzu</h3> -->
<!--         <h3>Rush</h3> -->
<!--         <h3>Topical</h3> -->
<!--     </div> -->
<!---->
<!--     <div class="photos"> -->
<!--         <img src="https://via.placeholder.com/150" alt="Lyr"> -->
<!--         <img src="https://via.placeholder.com/150" alt="Yuzu"> -->
<!--         <img src="https://via.placeholder.com/150" alt="Rush"> -->
<!--         <img src="https://via.placeholder.com/150" alt="Topical"> -->
<!--     </div> -->
<!-- </div> -->

<style lang="scss">
    .project-names {
        display: flex;
        flex-direction: column;
        // justify-content: center;
        align-items: center;
    }

    .photos {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .photos img {
        margin: 1em;
    }

    .project-list {
        display: flex;
        flex-wrap: wrap;
    }

    .project {
        flex-basis: 33%;
        margin: 1rem;
        padding: 1rem;
        background-color: #f7f7f7;
        border-radius: 0.5rem;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        text-align: center;
    }

    .project h2 {
        font-size: 1.5rem;
        font-weight: 700;
        margin-bottom: 0.5;
    }
</style>
