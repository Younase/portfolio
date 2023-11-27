<script>
    import viewport from '$lib/useViewportAction';
    import { fly } from 'svelte/transition';
    import { cubicOut } from 'svelte/easing';
    import skills from '$lib/content/skills.json';

    let visible;
</script>

<div class="tile is-child"
     use:viewport
     on:enterViewport={() => visible=1}
     on:exitViewport={() => visible=0}>
     {#key visible}
     <div class="box" in:fly={{x: 200, delay:200, duration:1000, easing:cubicOut }}>
         <h5 class="title is-5">
             Skills
         </h5>
         <div class="tags are-medium">
            {#each skills as skill}
                <span class="tag">{skill.name}</span>
            {/each}
         </div>
     </div>
     {/key}
</div>

<style>
</style>
