<script>
import CardApp from './CardApp.vue';
import products from '../assets/data/db.json';


export default {
    name: 'MainApp',

    data() {
        return {
            products: products.products,
        }
    },

    components: {
        CardApp,
    }
}
</script>

<template>
    <div class="container">
        <div class="row">

            <CardApp v-for="product in products" :product="product">
            </CardApp>
        </div>
    </div>
</template>

<style>
.label {

    font-size: 0.85em;
    color: white;
    font-weight: bold;
    padding: 3px 8px;
}

.red-label {
    background-color: red;
}

.green-label {
    background-color: green;
}

.brand {
    font-size: 0.75em;
}

.clothes-name {
    font-weight: bold;
}

.prices {
    font-size: 0.80em;
}

.discount-price {
    color: red;
    font-weight: bold;
}

.original-price {
    text-decoration: line-through;
}
</style>