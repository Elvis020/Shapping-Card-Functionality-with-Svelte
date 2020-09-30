<script>
	import CompCart from './CompCart.svelte';
	import CompNav from './CompNav.svelte';
	import CompProducts from './CompProducts.svelte';
	export let name;
</script>

<main>
	<CompNav />
	<CompProducts />
	<!-- <h1>Hello {name}!</h1> -->
	<CompCart />
</main>

<style>
</style>