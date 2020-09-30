<script>
	import CompCartProduct from './CompCartProduct.svelte';
    import { cartProducts } from './cart.js';
</script>


<style>
    /* your styles go here */
</style>

<h1>CART</h1>

{#each $cartProducts as product }
    <CompCartProduct {product} />
{/each}

