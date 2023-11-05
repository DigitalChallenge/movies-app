<script>
	import Search from '$lib/components/common/Search.svelte';
	import Pagination from '../common/Pagination.svelte';
	import FilmCard from './FilmCard.svelte';
</script>

<div class="films">
	<div class="container mx-auto">
		<div class="flex items-center justify-between mb-[30px]">
			<h2>Все фильмы</h2>
			<Search />
		</div>
		<div class="films__grid">
			<FilmCard />
			<FilmCard />
			<FilmCard />
			<FilmCard />
			<FilmCard />
			<FilmCard />
		</div>
		<div class="flex justify-center tablet:justify-end">
			<Pagination />
		</div>
	</div>
</div>

<style lang="scss">
	.films {
		background: black;
		color: white;
		padding: 50px 0;
		border-top: 1px solid var(--light);
	}
	.films__grid {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		gap: 30px;
		margin-bottom: 30px;
		@media (max-width: theme('screens.desktop')) {
			grid-template-columns: repeat(3, 1fr);
		}
		@media (max-width: theme('screens.laptop')) {
			grid-template-columns: repeat(2, 1fr);
		}
		@media (max-width: theme('screens.tablet')) {
			grid-template-columns: 1fr;
		}
	}
</style>
