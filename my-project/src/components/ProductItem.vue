<template>
    <div>
        <h3>{{ product.name }}</h3>
        <p>Price: ${{ product.price}}</p>
    </div>
</template>

<script>
export default {
    name: 'ProductItem',
    props: {
        product: {
            type: Object,
            required: true,
        }
    }
}
</script>