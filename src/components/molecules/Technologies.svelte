<script>
    import viewport from '$lib/useViewportAction';
    import { fly } from 'svelte/transition';
    import { cubicOut } from 'svelte/easing';
    import technologies from '$lib/content/technologies.json';

    let visible;
</script>

<div class="tile is-child"
     use:viewport
     on:enterViewport={() => visible=1}
     on:exitViewport={() => visible=0}>
     {#key visible}
     <div class="box" in:fly={{x: 200, delay:200, duration:1000, easing:cubicOut }}>
         <h5 class="title is-5">
             Technologies
         </h5>
         <div class="tags are-medium">
            {#each technologies as technology}
                <span class="tag">{technology.name}</span>
            {/each}
         </div>
     </div>
     {/key}
</div>

<style>
</style>
