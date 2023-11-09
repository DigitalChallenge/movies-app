<script lang="ts">
	import type { IFilm } from '../../database/films';

	export let film: IFilm;

	$: genres = film.genres.map((i) => i.name);
	$: countries = film.countries.map((i) => i.name);
	$: directors = film.persons.filter((i) => i.enProfession === 'director').map((i) => i.name);
</script>

<div class="container mx-auto">
	<div class="film-info">
		<div class="film-info__details">
			<h1>{film.name}</h1>
			<div>
				<div>
					<b>Год: </b>{film.year}
				</div>
				<div>
					<b>Жанр: </b>{genres.join(', ')}
				</div>
				<div>
					<b>Страна: </b>{countries.join(', ')}
				</div>
				<div>
					<b>{directors.length > 1 ? 'Режиссеры' : 'Режиссер'}: </b>{directors.join(', ')}
				</div>
			</div>
			<div class="film-info__description">
				{film.shortDescription}
			</div>
			<div class="film-info__rate">
				<div class="flex items-center gap-2">
					<img src="/icons/kp.svg" alt="kp" />
					{film.rating.kp.toFixed(1)}
				</div>
				<div class="flex items-center gap-2">
					<img src="/icons/imdb.svg" alt="imdb" />
					{film.rating.imdb.toFixed(1)}
				</div>
			</div>
		</div>
		<div class="film-info__img">
			<img src={film.backdrop.url} alt={film.name} />
		</div>
	</div>
</div>

<style lang="scss">
	.film-info {
		display: grid;
		grid-template-columns: 40% 60%;
		padding: 65px 0;
		@media (max-width: theme('screens.desktop')) {
			display: flex;
			flex-direction: column-reverse;
			gap: 50px;
			padding: 30px 0;
		}
	}
	.film-info__details {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		font-size: 18px;
		padding-right: 50px;
		@media (max-width: theme('screens.desktop')) {
			gap: 30px;
		}
	}
	.film-info__rate {
		display: flex;
		align-items: center;
		gap: 30px;
	}
	.film-info__img {
		border-radius: 20px;
		overflow: hidden;
		img {
			width: 100%;
		}
	}
</style>
