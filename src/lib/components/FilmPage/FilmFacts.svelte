<script lang="ts">
	import type { IFilm } from '../../database/films';

	export let film: IFilm;
	$: facts = film.facts.map((i) => i.value);
</script>

<div class="film-facts__wrapper">
	<div class="container mx-auto">
		<h2 class="mb-7">Факты о фильме</h2>
		<ul class="film-facts">
			{#each facts as fact}
				<li class="film-facts__item">
					{@html fact}
				</li>
			{/each}
		</ul>
	</div>
</div>

<style>
	.film-facts__wrapper {
		padding: 60px 0;
		border-top: 1px solid var(--light);
	}
	.film-facts {
		display: flex;
		flex-direction: column;
		gap: 25px;
	}
	.film-facts__item {
		padding: 30px;
		border: 1px solid var(--light);
		border-radius: 15px;
	}
</style>
