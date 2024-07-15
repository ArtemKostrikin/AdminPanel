<template>
    <div>
        <h2>Add/Edit Product</h2>
        <form @submit.prevent="handleSubmit">
            <label>Name:</label>
            <input v-model="productName" type="text" />
            <label>Price:</label>
            <input v-model.number="productPrice" type="number" />
            <button type="submit">Save</button>
        </form>
    </div>
</template>

<script>
export default {
    name: 'ProductForm',
    data() {
        return {
            productName: '',
            productPrice: 0,
        };
    },
    methods: {
        handleSubmit() {
            const newProduct = {
                name: this.productName,
                price: this.productPrice,
            };
            console.log('New Product:', newProduct);
            this.productName = '';
            this.productPrice = '';
        },
    },
};
</script>
