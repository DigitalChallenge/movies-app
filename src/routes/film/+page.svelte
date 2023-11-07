<script>
	import FilmActors from '$lib/components/FilmPage/FilmActors.svelte';
	import FilmDescription from '$lib/components/FilmPage/FilmDescription.svelte';
	import FilmFacts from '$lib/components/FilmPage/FilmFacts.svelte';
	import FilmInfo from '$lib/components/FilmPage/FilmInfo.svelte';
	import Navbar from '$lib/components/Header/Navbar.svelte';
</script>

<div class="film-page">
	<Navbar />
	<FilmInfo />
	<FilmDescription />
	<FilmActors />
	<FilmFacts />
</div>

<style>
	.film-page {
		background-color: black;
		color: white;
	}
</style>
