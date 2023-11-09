<script lang="ts">
	import { onMount } from 'svelte';
	import { register, type SwiperContainer } from 'swiper/element/bundle';
	import type { SwiperOptions } from 'swiper/types';
	import ActorCard from './ActorCard.svelte';
	import type { IFilm } from '../../database/films';
	export let film: IFilm;
	$: actors = film.persons.filter((i) => i.enProfession === 'actor');

	register();
	let swiperEl: SwiperContainer;

	const swiperParams: SwiperOptions = {
		slidesPerView: 2,
		spaceBetween: 60,
		loop: true,
		autoplay: {
			delay: 3000
		},
		breakpoints: {
			1440: {
				slidesPerView: 7
			},
			1024: {
				slidesPerView: 5
			},
			640: {
				slidesPerView: 3
			}
		}
	};

	onMount(() => {
		Object.assign(swiperEl, swiperParams);
		swiperEl.initialize();
	});
</script>

<div class="film-actors">
	<div class="container mx-auto">
		<h2 class="mb-7">Актеры</h2>
		<swiper-container bind:this={swiperEl} init="false">
			{#each actors as actor}
				<swiper-slide><ActorCard person={actor} /></swiper-slide>
			{/each}
		</swiper-container>
	</div>
</div>

<style>
	.film-actors {
		padding-bottom: 65px;
	}
</style>
