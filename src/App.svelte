<script>
	import Header from './components/layout/Header.svelte'
	import About from './components/layout/About.svelte'
	import Services from './components/layout/Services.svelte'
	import ClientTestimonials from './components/layout/ClientTestimonials.svelte'
	import Gallery from './components/layout/Gallery.svelte'
	import Footer from './components/layout/Footer.svelte'
</script>

<div class="container">
	<Header/>
	<main>
		<About/>
		<Services/>
		<ClientTestimonials/>
		<Gallery/>
	</main>
	<Footer/>
</div>

<style>
	.container {
		max-width: 93.75rem;
		margin: 0 auto;
		box-shadow: 0rem 0rem 6rem -3rem rgba(0, 0, 0, .3);
	}
</style>