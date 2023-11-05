<script>
	import RecentCard from './RecentCard.svelte';
</script>

<div class="recents">
	<div class="container mx-auto">
		<h2 class="recents__title">Продолжить просмотр</h2>
		<div class="recents__items">
			<RecentCard />
			<RecentCard />
			<RecentCard />
			<RecentCard />
		</div>
	</div>
</div>

<style>
	.recents {
		background: black;
		color: white;
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
