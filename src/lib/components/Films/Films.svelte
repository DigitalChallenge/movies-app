<script>
	import Pagination from '../common/Pagination.svelte';
	import Search from '../common/Search.svelte';
	import FilmCard from './FilmCard.svelte';
</script>

<div class="films">
	<div class="container mx-auto">
		<div class="films__top">
			<h2 class="films__title">Все фильмы</h2>
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
		<div class="flex justify-center mt-[40px] tablet:justify-end">
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
		@media (max-width: theme('screens.tablet')) {
			padding: 10px;
		}
	}
	.films__top {
		display: flex;
		justify-content: space-between;
		align-items: center;
		margin-bottom: 30px;
	}
	.films__grid {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		gap: 25px;
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
