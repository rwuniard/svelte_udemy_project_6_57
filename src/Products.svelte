<script>
    import { createEventDispatcher } from 'svelte';
    export let productTitle;

    const dispatch = createEventDispatcher();

    function addToCart() {
        // The 'add-to-cart' is the name of the event.
        dispatch('add-to-cart', { id: 'p1' }); // you can put data into the second parameter to pass additional information, such as string, number, object, etc.
    }

    function delSomething() {
        dispatch('delete-something', 'deleting product');
    }
</script>

<article>
    <h1>{productTitle}</h1>
    <button on:click={addToCart}>Add to Cart</button>
    <button on:click={delSomething}>Delete</button>
</article>
