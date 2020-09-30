<script>
	import { cartProducts } from './cart.js';
    export let product;
    let disabled = false
    

    // Adding a product
    const addProduct = () => {
        product.quantity++
        $cartProducts = $cartProducts
    }
    // Subing a product
    const subProduct = () => {
        if (product.quantity == 0) disabled = true
        if (product.quantity > 0){
            product.quantity--
            $cartProducts = $cartProducts
        }
    }
    // Removing a product
    const rmProduct = () => {
        $cartProducts = $cartProducts.filter(item => product.id != item.id)
    }
</script>


<style>
    /* your styles go here */
</style>

<div class="product">
    Name : {product.name}
    Price : {product.price}
    Units : {product.quantity}
    <button on:click={addProduct} >+</button>
    <button on:click={subProduct} {disabled} >-</button>
    <button on:click={rmProduct} >Remove Product</button>
</div>

