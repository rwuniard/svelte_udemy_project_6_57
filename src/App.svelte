<script>
    import Product from './Products.svelte';
</script>

<Product
    productTitle="My Product"
    on:add-to-cart={() => alert('Add to Cart Clicked')}
    on:delete-something={() => alert('delete clicked')}
/>
