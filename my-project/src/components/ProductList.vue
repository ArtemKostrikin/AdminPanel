<template>
    <div>
        <h2>Product List</h2>
        <ul>
            <li><div v-for="product in products" :key="product.id">
                {{ product.name }} - ${{ product.price }}
            </div>

            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'ProductList',
    data() {
        return {
            products: [
                {id: 1, name: 'Product 1', price: 10 },
                {id: 2, name: 'Product 2', price: 20 },
                {id: 3, name: 'Product 3', price: 30 }
            ],
        };
    },
};
</script>