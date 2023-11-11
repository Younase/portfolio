<script>
    import viewport from '$lib/useViewportAction';
    import { fly } from 'svelte/transition';
    import { cubicOut } from 'svelte/easing';

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
             <span class="tag">Python</span>
             <span class="tag">C</span>
             <span class="tag">Bash</span>
             <span class="tag">Java</span>
             <span class="tag">Javascript</span>
         </div>
     </div>
     {/key}
</div>

<style>
</style>
