<script lang="ts">
	import type { IPerson } from '../../database/films';

	export let person: IPerson;
</script>

<div class="actor-card">
	<img class="actor-card__img" src={person.photo} alt="actor-name" />
	<p class="actor-card__name">{person.name}</p>
</div>

<style>
	.actor-card__img {
		width: 100%;
		border-radius: 15px;
		margin-bottom: 10px;
	}
	.actor-card__name {
		text-align: center;
	}
</style>
