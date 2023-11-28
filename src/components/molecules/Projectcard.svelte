<script>
    // basic card componenet w/ popup modal
    // TODO make modal popup

    import viewport from '$lib/useViewportAction';
    import { fly } from 'svelte/transition';
    import { cubicOut } from 'svelte/easing';

export let title;
export let description;
export let body;
export let is_modal=false;
export let showModal=false;
let visible;
$:visible=showModal;
</script>

<div class="projectcard" use:viewport
     on:enterViewport={() => visible=1}
     on:exitViewport={() => visible=0}
     >
     <div class="{is_modal?'modal':''} {showModal?'is-active':''}">
         {#if is_modal}
         <div class="modal-background"></div>
         {/if}
         <div class="block">
         {#key visible}
         <div class="card" in:fly={{y: 200, delay: 200, duration:Math.floor(500+700*Math.random()), easing:cubicOut }}>
             <div class="card-image">
                 <figure class="image">
                     <img src="https://bulma.io/images/placeholders/640x360.png" alt="Placeholder image">
                 </figure>
                 {#if is_modal}
                <button class="delete is-overlay" aria-label="close" on:click={() => (showModal = !showModal)}></button>
                 {/if}
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
</div>

<style>
</style>
