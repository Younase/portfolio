<script>
    import Projectcard from '../molecules/Projectcard.svelte';

    let projects =[
            { name: 'project1', description: 'lorem ipsum dolor', url: 'link.com/p1', image_url: 'link.com/url1' },
            { name: 'project2', description: 'lorem ipsum dolor', url: 'link.com/p2', image_url: 'link.com/url2' },
            { name: 'project3', description: 'lorem ipsum dolor', url: 'link.com/p3', image_url: 'link.com/url3' },
            { name: 'project1', description: 'lorem ipsum dolor', url: 'link.com/p1', image_url: 'link.com/url1' },
            { name: 'project2', description: 'lorem ipsum dolor', url: 'link.com/p2', image_url: 'link.com/url2' },
            { name: 'project3', description: 'lorem ipsum dolor', url: 'link.com/p3', image_url: 'link.com/url3' }
        ]
</script>

<section class="section" id="projects">
    <div class="container is-max-desktop">
        <div class="block">
            <h1 class="title has-text-white">
                Projects
            </h1>
        </div>
        <div class="columns is-multiline">
            {#each projects as project, i}
                <Projectcard title={project.name} />
            {/each}
        </div>
    </div>


</section>
<style>

</style>
