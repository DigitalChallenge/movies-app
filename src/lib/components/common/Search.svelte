<script lang="ts">
	import { createEventDispatcher } from 'svelte';
	import { debounce } from 'lodash';
	const handler = debounce(() => {
		dispatch('input', val);
	}, 500);
	const dispatch = createEventDispatcher();
	let val = '';
</script>

<div class="search">
	<img class="search__img" src="/icons/search.svg" alt="search" />
	<input
		class="search__input"
		type="text"
		placeholder="Поиск"
		bind:value={val}
		on:input={handler}
	/>
</div>

<style>
	.search {
		display: flex;
		align-items: center;
		background: #f4f6f9;
		width: fit-content;
		border-radius: 10px;
		overflow: hidden;
	}
	.search__img {
		padding: 0 5px;
	}
	.search__input {
		background: none;
		padding: 10px;
		color: black;
	}
	.search__input:focus-visible {
		outline: none;
	}
</style>
