<script>
    import { cartProducts } from './cart.js';
    let itemsInCart = 0

    // Creating a reactive value to update in the nav
    $: {
        let count = 0
        for(let item of $cartProducts){
            count += item.quantity
        }
        itemsInCart = count
    }
</script>


<style>
    /* your styles go here */
</style>

<nav>
    <a href="/">Home</a>
    <a href="/contact-us">Contact Us</a>
    Items in cart {itemsInCart}
</nav>