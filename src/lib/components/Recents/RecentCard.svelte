<script lang="ts">
	import type { IFilm } from '../../database/films';

	export let film: IFilm;
</script>

<div>
	<div class="recent-card" style="background: url({film.backdrop.previewUrl})no-repeat top;">
		<div class="recent-card__progress">
			<div class="recent-card__progress-fill" style="width: {film.seen}%;" />
		</div>
	</div>
	<div class="recent-card__name">{film.name}</div>
</div>

<style>
	.recent-card {
		height: 200px;
		background-size: cover;
		position: relative;
	}
	.recent-card__progress {
		background: rgba(255, 255, 255, 0.5);
		height: 6px;
		position: absolute;
		bottom: 0;
		left: 0;
		right: 0;
	}
	.recent-card__progress-fill {
		background: var(--primary);
		height: 6px;
	}
	.recent-card__name {
		padding-left: 20px;
		position: relative;
		padding-top: 10px;
		padding-bottom: 10px;
	}
	.recent-card__name::before {
		content: '';
		display: block;
		width: 10px;
		height: 10px;
		border-radius: 50%;
		background: var(--primary);
		position: absolute;
		left: 0;
		top: 50%;
		transform: translateY(-50%);
	}
</style>
