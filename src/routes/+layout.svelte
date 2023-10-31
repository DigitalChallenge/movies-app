<script>
	import '../assets/app.css';
	import DcHeader from '$lib/components/Header/DCHeader.svelte';
	import Footer from '$lib/components/Footer.svelte';
</script>

<DcHeader />
<slot />
<Footer />

<style>
</style>
