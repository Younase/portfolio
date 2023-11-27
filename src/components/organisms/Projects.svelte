<script>
    import Projectcard from '../molecules/Projectcard.svelte';
    import projects from "$lib/content/projects.json";

</script>

<section class="section" id="projects">
    <div class="container is-max-desktop">
        <div class="block">
            <h1 class="title">
                Projects
            </h1>
        </div>
        <div class="columns is-multiline">
            {#each projects as project}
                <Projectcard title={project.name} />
            {/each}
        </div>
    </div>


</section>
<style>

</style>
