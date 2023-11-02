<script>
	import DcButton from '../common/DCButton.svelte';
</script>

<div class="navbar">
	<div class="container mx-auto flex items-center justify-between">
		<img src="/LOGO.svg" alt="Logo" />
		<DcButton>Войти</DcButton>
	</div>
</div>

<style lang="scss">
	.navbar {
		background: rgba(0, 0, 0, 0.5);
		padding: 10px 0;
		@media (max-width: theme('screens.tablet')) {
			padding: 10px;
		}
	}
</style>
