<ul class="pagination">
	<li>
		<a class="pagination__item-link" href="/">
			<img src="/icons/left.svg" alt="Left" />
		</a>
	</li>
	<li>
		<a class="pagination__item-link pagination__item-link_active" href="/"> 1 </a>
	</li>
	<li>
		<a class="pagination__item-link" href="/"> 2 </a>
	</li>
	<li>
		<a class="pagination__item-link" href="/"> 3 </a>
	</li>
	<li>
		<a class="pagination__item-link" href="/"> 4 </a>
	</li>
	<li>
		<a class="pagination__item-link" href="/">
			<img src="/icons/right.svg" alt="Right" />
		</a>
	</li>
</ul>

<style>
	.pagination {
		display: flex;
		border: 1px solid var(--light);
		width: fit-content;
		border-radius: 30px;
	}
	.pagination__item-link {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 50px;
		height: 50px;
	}
	.pagination__item-link_active {
		color: var(--primary);
	}
	.pagination__item-link:hover {
		color: var(--primary);
	}
</style>
