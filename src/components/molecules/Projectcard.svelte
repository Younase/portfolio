<script>
    // basic card componenet w/ popup modal
    // TODO make modal popup

    import viewport from '$lib/useViewportAction';
    import { fly } from 'svelte/transition';
    import { cubicOut } from 'svelte/easing';

    export let title;
    let visible;
</script>

<div class="projectcard column is-6" use:viewport
     on:enterViewport={() => visible=1}
     on:exitViewport={() => visible=0}
     >
     <div class="block">
         {#key visible}
         <div class="card" in:fly={{y: 200, delay: 200, duration:Math.floor(500+700*Math.random()), easing:cubicOut }}>
             <div class="card-image">
                 <figure class="image">
                     <img src="https://bulma.io/images/placeholders/640x360.png" alt="Placeholder image">
                 </figure>
             </div>
             <div class="card-content">
                 <div class="media-content">
                     <p class="subtitle is-4">
                     {title}
                     </p>
                 </div>
                 <p class="content">
                 article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd 
                 article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd 
                 </p>
             </div>
         </div>
         {/key}
     </div>
</div>

<style>
</style>
