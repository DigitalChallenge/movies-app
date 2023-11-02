<script lang="ts">
	import RecentCard from './RecentCard.svelte';
	import { onMount } from 'svelte';
	import { register, type SwiperContainer } from 'swiper/element/bundle';
	import type { SwiperOptions } from 'swiper/types';
	register();
	let swiperEl: SwiperContainer;

	const swiperParams: SwiperOptions = {
		slidesPerView: 1,
		spaceBetween: 20,
		injectStyles: [
			`
			.swiper {
				overflow: visible;
			}
		`
		],
		breakpoints: {
			640: {
				slidesPerView: 2
			},
			1024: {
				slidesPerView: 3
			},
			1440: {
				slidesPerView: 4
			}
		}
	};

	onMount(() => {
		Object.assign(swiperEl, swiperParams);
		swiperEl.initialize();
	});
</script>

<div class="recents">
	<div class="container mx-auto">
		<h2 class="recents__title">Продолжить просмотр</h2>

		<swiper-container init="false" bind:this={swiperEl}>
			<swiper-slide><RecentCard /></swiper-slide>
			<swiper-slide><RecentCard /></swiper-slide>
			<swiper-slide><RecentCard /></swiper-slide>
			<swiper-slide><RecentCard /></swiper-slide>
			<swiper-slide><RecentCard /></swiper-slide>
			<swiper-slide><RecentCard /></swiper-slide>
			<swiper-slide><RecentCard /></swiper-slide>
			<swiper-slide><RecentCard /></swiper-slide>
		</swiper-container>
	</div>
</div>

<style lang="scss">
	.recents {
		background: black;
		color: white;
		padding-bottom: 50px;
		@media (max-width: theme('screens.tablet')) {
			padding: 10px;
		}
	}
	.recents__title {
		font-size: 20px;
		font-weight: 500;
		padding: 25px 0;
	}
</style>
