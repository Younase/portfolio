<script>
    import { page } from '$app/stores';
import logo from '$lib/images/svelte-logo.svg';
import github from '$lib/images/github.svg';
import 'iconify-icon'

let open=0;
</script>

<header>
    <nav class="navbar is-fixed-top container">
        <div class="navbar-brand">
            <a class="navbar-item" href="https://kit.svelte.dev">
                <img src={logo} alt="SvelteKit" />
            </a>

            <a on:click={()=>{open = !open}} 
                role="button" 
                class="navbar-burger {open == 1 ? 'is-active':''}" 
                aria-label="menu" 
                aria-expanded="false" 
                data-target="navbarBasicExample"
                >
                <span aria-hidden="true"></span>
                <span aria-hidden="true"></span>
                <span aria-hidden="true"></span>
            </a>
        </div>


        <div class="navbar-menu {open == 1 ? 'is-active':''}">
            <div class="navbar-start is-flex-grow-1 is-justify-content-center">

                {#each ['Home', 'About', 'Projects', 'Experience', 'Contact'] as link, i}
                    <a class="navbar-item" href="#{link.toLowerCase()}">{link}</a>
                {/each}
            </div>

            <div class="navbar-end">
                <a class="navbar-item" href="mailto:email@example.com">
                    <iconify-icon icon="line-md:email" height="auto"></iconify-icon>
                </a>
                <a class="navbar-item" href="https://www.github.com/younase">
                    <iconify-icon icon="line-md:github" height="auto"></iconify-icon>
                </a>
                <a class="navbar-item" href="https://www.linkedin.com">
                    <iconify-icon icon="line-md:linkedin" height="auto"></iconify-icon>
                </a>
            </div>
    </nav>


</header>

<style>
</style>
