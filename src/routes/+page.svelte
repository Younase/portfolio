<script>
	import Home from '../components/organisms/Home.svelte';
	import About from '../components/organisms/About.svelte';
	import Projects from '../components/organisms/Projects.svelte';
	import Experience from '../components/organisms/Experience.svelte';
	import Contact from '../components/organisms/Contact.svelte';
	import Background from '../components/organisms/Background.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="wrapper">
    <Background />
    <Home />
    <About />
    <Projects />
    <Experience />
    <Contact />
</div>
<style lang="scss">
    .wrapper{
        position: relative;
    }
</style>
