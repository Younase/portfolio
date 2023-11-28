<script>
    // basic card componenet w/ popup modal
    // TODO make modal popup

    import 'iconify-icon';
    import viewport from '$lib/useViewportAction';
    import { fly } from 'svelte/transition';
    import { cubicOut } from 'svelte/easing';

    export let title;
    export let description;
    export let body;
    export let link;
    export let img_url;
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
                         <img src={img_url} alt="Placeholder image">
                     </figure>
                     {#if is_modal}
                         <button class="delete is-overlay" aria-label="close" on:click={() => (showModal = !showModal)}></button>
                     {/if}
                 </div>
                 <div class="card-content">
                     <div class="media">

                         <div class="media-content">
                             <p class="title is-4">
                                 {title}
                             </p>
                         </div>
                         <a href={link}>
                         <div class="media-left is-clickable">
                                 <iconify-icon icon="line-md:github" height="auto"></iconify-icon>
                         </div>
                        </a>
                     </div>
                     <p class="content">
                         {description}
                     </p>
                 </div>
             </div>
             {/key}
         </div>
     </div>
</div>

<style>
</style>
