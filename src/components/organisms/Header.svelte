<script>
    import { page } from '$app/stores';
    import logo from '$lib/images/svelte-logo.svg';
    import github from '$lib/images/github.svg';

    let open=0;
    $: if (open){

        }
</script>

<header>
    <nav class="navbar is-fixed-top is-dark">
        <div class="navbar-brand">
            <a class="navbar-item" href="https://kit.svelte.dev">
                <img src={logo} alt="SvelteKit" />
            </a>

            <a on:click={()=>{open = !open}} role="button" class="navbar-burger {open == 1 ? 'is-active':''}" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
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
                <div class="navbar-item">
                    <a href="https://github.com/sveltejs/kit">
                        <img src={github} alt="GitHub" />
                    </a>
                </div>
            </div>
    </nav>


</header>

<style>

</style>
