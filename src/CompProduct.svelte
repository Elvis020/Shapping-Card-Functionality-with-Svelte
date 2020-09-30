<script>
    import {cartProducts} from './cart.js';
    export let product = {};
    const buyProduct = () => {
        // Looping through the products to check if it is already there
        for (let item of $cartProducts) {
            if(item.id == product.id){
                item.quantity++
                $cartProducts = $cartProducts
                return
            }
        }
        product.quantity = 1;
        console.log(product.quantity);
        // Adding a product to the already existing cart store
        $cartProducts = [...$cartProducts, product]

        
    }
</script>


<style>
    /* your styles go here */
    button {
        cursor: pointer;
    }
</style>

<div class="product">
    id: {product.id}
    name: {product.name}
    price: {product.price}
<button on:click={buyProduct}>Buy &#x1F6D2;</button>
</div>