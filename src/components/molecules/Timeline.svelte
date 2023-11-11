<script>
    import viewport from '$lib/useViewportAction';
    import { fly } from 'svelte/transition';
    import { cubicOut } from 'svelte/easing';

    let visible;
</script>
<div use:viewport
     on:enterViewport={() => visible=1}
     on:exitViewport={() => visible=0}>
     {#key visible}              

     <div class="tile is-child box" in:fly={{x: -200, delay:200, duration:1000, easing:cubicOut }}>
         <div class="timeline">
             <div class="timeline-item content">
                 <h5 class="title is-5 is-marginless">
                     Education 1
                 </h5>
                 <div class="subtitle is-6 is-marginless">
                     organization 1
                 </div>
                 <p class="content">
                 org text, description,...article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd
                 </p>
                 <ul>
                     <li>asdasdasdasdas</li>
                     <li>asdasdasdasdas</li>
                     <li>asdasdasdasdas</li>
                     <li>asdasdasdasdas</li>
                 </ul>
             </div>

             <div class="timeline-item content">
                 <h5 class="title is-5 is-marginless">
                     Education 2
                 </h5>
                 <div class="subtitle is-6 is-marginless">
                     organization 2
                 </div>
                 <p class="content">
                 org text, description,...article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd
                 </p>
                 <ul>
                     <li>asdasdasdasdas</li>
                     <li>asdasdasdasdas</li>
                     <li>asdasdasdasdas</li>
                     <li>asdasdasdasdas</li>
                 </ul>
             </div>

             <div class="timeline-item content">
                 <h5 class="title is-5 is-marginless">
                     Education 3
                 </h5>
                 <div class="subtitle is-6 is-marginless">
                     organization 3
                 </div>
                 <p class="content">
                 org text, description,...article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd article bodyasdbkhajb kjb jkbkdjabsdba kjbaksdbajsbd
                 </p>
                 <ul>
                     <li>asdasdasdasdas</li>
                     <li>asdasdasdasdas</li>
                     <li>asdasdasdasdas</li>
                     <li>asdasdasdasdas</li>
                 </ul>
             </div>

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
