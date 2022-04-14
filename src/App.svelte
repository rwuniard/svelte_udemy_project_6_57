<script>
    import Product from './Products.svelte';
    import Modal from './Modal.svelte';

    let products = [
        {
            id: '01',
            title: 'A book',
            price: 9.99,
        },
    ];
    function addToCart(event) {
        console.log(event);
    }

    function deleteSomething(event) {
        console.log(event.detail);
    }
</script>

{#each products as product}
    <!-- These two lines were inside the <Product -->
    <!-- title={product.title} -->
    <!-- price={product.price} -->
    <!-- the two statements above can be re-written with spread operator below assuming the props name are matching -->
    <Product {...product} on:add-to-cart={addToCart} on:delete-something={deleteSomething} />
{/each}

<Modal>
    <h1 slot="header">Hello Slot</h1>
    <h2>This really works!</h2>
    <button slot="footer">Confirm</button>
</Modal> />
