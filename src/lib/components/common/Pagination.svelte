<script lang="ts">
	export let maxPage: number;
	export let currentPage: number;
</script>

<ul class="pagination">
	<li>
		<a class="pagination__item" href="/?page={currentPage - 1}#title"
			><img src="/icons/left.svg" alt="left" /></a
		>
	</li>
	{#each Array(maxPage) as _, idx}
		<li>
			<a
				class="pagination__item"
				class:pagination__item_active={currentPage === idx + 1}
				href="/?page={idx + 1}#title">{idx + 1}</a
			>
		</li>
	{/each}
	<!-- <li>
		<a class="pagination__item pagination__item_active" href="/">1</a>
	</li>
	<li>
		<a class="pagination__item" href="/">2</a>
	</li>
	<li>
		<a class="pagination__item" href="/">3</a>
	</li>
	<li>
		<a class="pagination__item" href="/">4</a>
	</li> -->
	<li>
		<a class="pagination__item" href="/?page={currentPage + 1}#title">
			<img src="/icons/right.svg" alt="right" />
		</a>
	</li>
</ul>

<style>
	.pagination {
		border: 1px solid var(--light);
		border-radius: 20px;
		display: flex;
	}
	.pagination__item {
		width: 50px;
		height: 50px;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.pagination__item_active {
		color: var(--primary);
	}
	.pagination__item:hover {
		color: var(--primary);
	}
</style>
