<script>
	import Home from '../components/organisms/Home.svelte';
	import About from '../components/organisms/About.svelte';
	import Projects from '../components/organisms/Projects.svelte';
	import Experience from '../components/organisms/Experience.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>


    <Home />
    <About />
    <Projects />
    <Experience />
<style>
    /*
       :global(body){
        background-color: #F6F6F6;
       }
       */
</style>
