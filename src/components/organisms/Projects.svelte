<script>
    import Projectcard from '../molecules/Projectcard.svelte';
    import projects from "$lib/content/projects.json";

    let showModals=new Array(projects.length).fill(false);
</script>

<section class="section" id="projects">
    <div class="container is-max-desktop">
        <div class="block">
            <h1 class="title">
                Projects
            </h1>
        </div>
        <div class="columns is-multiline">
            {#each projects as project,i}
                <div class="column is-6"> <!-- on:click={() => (showModals[i] = true)}> -->
                    <Projectcard  title={project.name} link={project.link} img_url={project.img_url} description={project.description}/>
                </div>
                <div class="modal" class:is-active={showModals[i]}>
                    <div class="modal-background"></div>
                    <Projectcard title={project.name} link={project.link} img_url={project.img_url} description={project.description} is_modal=true bind:showModal={showModals[i]}/>
                </div>
            {/each}
        </div>
    </div>


</section>
<style>
</style>
