<script>
    import Product from './Products.svelte';

    function addToCart(event) {
        console.log(event);
    }

    function deleteSomething(event) {
        console.log(event.detail);
    }
</script>

<Product productTitle="My Product" on:add-to-cart={addToCart} on:delete-something={deleteSomething} />
