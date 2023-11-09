<script>
	import DcButton from '../common/DCButton.svelte';
</script>

<div class="navbar">
	<div class="container mx-auto flex items-center justify-between">
		<a href="/"><img src="/LOGO.svg" alt="Logo" /></a>
		<DcButton>Войти</DcButton>
	</div>
</div>

<style>
	.navbar {
		background: rgba(0, 0, 0, 0.5);
		padding: 10px 0;
	}
</style>
