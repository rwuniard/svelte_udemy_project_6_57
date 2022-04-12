<script>
    import Product from './Products.svelte';
</script>

<Product productTitle="My Product" on:click={() => alert('Clicked')} />
