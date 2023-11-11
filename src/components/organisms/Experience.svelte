<script>
    import Timeline from '../molecules/Timeline.svelte'
    import Skills from '../molecules/Skills.svelte'
    import Technologies from '../molecules/Technologies.svelte'
    import Certificates from '../molecules/Certificates.svelte'
</script>

<section class="section" id="experience">
    <div class="container">
        <div class="block">
            <h1 class="title">
                Experience
            </h1>
        </div>     

        <div class="tile is-ancestor">
            <div class="tile is-8 is-parent">
                <Timeline />
            </div>
            <div class="tile is-parent is-vertical">
                <Skills />
                <Technologies />
                <Certificates />
            </div>
        </div>

    </div>
</section>

<style>
</style>
