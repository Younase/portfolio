<script>
    import viewport from '$lib/useViewportAction';
    import { fly } from 'svelte/transition';
    import { cubicOut } from 'svelte/easing';
    import experiences from '$lib/content/experiences.json';

    let visible;
</script>
<div class="tile is-child" use:viewport
     on:enterViewport={() => visible=1}
     on:exitViewport={() => visible=0}>
     {#key visible}              

     <div class="box" in:fly={{x: -200, delay:200, duration:1000, easing:cubicOut }}>
         <div class="timeline">
            {#each experiences as experience}
             <div class="timeline-item content">
                 <h5 class="title is-5 is-marginless">
                     {experience.position}
                 </h5>
                 <span class="subtitle is-6 is-marginless">
                     {experience.company}
                 </span>
                 <span class="subtitle is-7 is-marginless">
                     {experience.timeframe}
                 </span>
                 <p class="content">
                    {experience.description.body}
                 </p>
                 <ul>
            {#each experience.description.bulletpoints as bulletpoint}
                <li>{bulletpoint}</li>
            {/each}
                 </ul>
             </div>
            {/each}


         </div>

     </div>
     {/key}
</div>
<style>
    .timeline {
        position: relative;
        padding-left: 80px;
    }

    .timeline::before {
        content: '';
        background: grey;
        display: inline-block;
        position: absolute;
        left: 33px;
        width: 1px;
        height: 100%;
        z-index: 10;
    }

    .timeline-item::before {
        content: '';
        background: white;
        border: 2px solid black;
        border-radius: 10px;
        display: inline-block;
        position: absolute;
        margin-top: 5px;
        left: 26px;
        width: 15px;
        height: 15px;
        z-index: 10;
    }

    .timeline-item:hover::before {
        background: black;
    } 
</style>
