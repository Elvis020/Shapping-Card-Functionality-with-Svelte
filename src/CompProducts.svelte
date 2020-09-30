<script>
	import CompProduct from './CompProduct.svelte';
    import { products } from './products.js';
    
</script>


<style>
    /* your styles go here */

</style>

<h1>PRODUCTS</h1>
{#each $products as product}
    <CompProduct {product}/>
{/each}
<!-- <CompProduct /> -->