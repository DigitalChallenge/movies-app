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
		loop: true,
		autoplay: {
			delay: 1000
		},
		injectStyles: [
			`
			.swiper {
				 overflow: visible;
			}
		`
		],
		breakpoints: {
			1440: {
				slidesPerView: 4
			},
			1024: {
				slidesPerView: 3
			},
			640: {
				slidesPerView: 2
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
		<!-- <div class="recents__items">
			<RecentCard />
			<RecentCard />
			<RecentCard />
			<RecentCard />
		</div> -->
		<swiper-container bind:this={swiperEl} init="false">
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

<style>
	.recents {
		background: black;
		color: white;
		overflow: hidden;
		padding-bottom: 50px;
	}
	.recents__title {
		font-size: 20px;
		font-weight: 500;
		padding: 25px 0;
	}
	.recents__items {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		gap: 30px;
	}
</style>
