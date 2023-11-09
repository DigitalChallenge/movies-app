<script lang="ts">
	import type { IRate } from '../../database/films';

	export let rate: IRate;
	export let img: string;

	let rateStatus: string = 'high';
	if (rate.kp < 7) {
		rateStatus = 'middle';
	}
	if (rate.kp < 4) {
		rateStatus = 'low';
	}
</script>

<div
	class="film-card"
	style:background={`url('${img}') no-repeat top`}
	style:background-size="cover"
>
	<div class="film-card__shadow">
		<span class="film-card__rate film-card__rate_{rateStatus}">{rate.kp.toFixed(1)}</span>
	</div>
</div>

<style>
	.film-card {
		height: 500px;
		border-radius: 10px;
	}
	.film-card__shadow {
		background: rgba(0, 0, 0, 0.8);
		padding: 5px 15px;
	}
	.film-card__rate {
		padding: 0 10px;
		border-radius: 3px;
	}
	.film-card__rate_high {
		background: var(--secondary);
	}
	.film-card__rate_middle {
		background: #cbc644;
	}
	.film-card__rate_low {
		background: #d49314;
	}
</style>
