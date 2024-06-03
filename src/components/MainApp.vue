<script>
import CardApp from './CardApp.vue';

export default {
    name: 'MainApp',

    data() {
        return {
            products: [
                {
                    "id": 1,
                    "frontImage": "1.webp",
                    "backImage": "1b.webp",
                    "brand": "Levi's",
                    "name": "Relaxed Fit",
                    "price": 29.99,
                    "isInFavorites": true,
                    "badges": [
                        {
                            "type": "tag",
                            "value": "Sostenibilità"
                        },
                        {
                            "type": "discount",
                            "value": "-50%"
                        }
                    ]
                },
                {
                    "id": 2,
                    "frontImage": "2.webp",
                    "backImage": "2b.webp",
                    "brand": "Guess",
                    "name": "Roses Tee",
                    "price": 20.99,
                    "isInFavorites": true,
                    "badges": [
                        {
                            "type": "discount",
                            "value": "-30%"
                        }
                    ]
                },
                {
                    "id": 3,
                    "frontImage": "3.webp",
                    "backImage": "3b.webp",
                    "brand": "Come Zucchero Filato",
                    "name": "Voglia di colori pastello",
                    "price": 129.99,
                    "isInFavorites": false,
                    "badges": [
                        {
                            "type": "discount",
                            "value": "-30%"
                        }
                    ]
                },
                {
                    "id": 4,
                    "frontImage": "4.webp",
                    "backImage": "4b.webp",
                    "brand": "Levi's",
                    "name": "Tee Unisex",
                    "price": 14.99,
                    "isInFavorites": false,
                    "badges": [
                        {
                            "type": "tag",
                            "value": "Sostenibilità"
                        },
                        {
                            "type": "discount",
                            "value": "-50%"
                        }
                    ]
                },
                {
                    "id": 5,
                    "frontImage": "5.webp",
                    "backImage": "5b.webp",
                    "brand": "Maya Deluxe",
                    "name": "Stripe Bodice",
                    "price": 99.99,
                    "isInFavorites": true,
                    "badges": [
                        {
                            "type": "tag",
                            "value": "Sostenibilità"
                        },
                        {
                            "type": "discount",
                            "value": "-50%"
                        }
                    ]
                },
                {
                    "id": 6,
                    "frontImage": "6.webp",
                    "backImage": "6b.webp",
                    "brand": "Esprit",
                    "name": "Maglione - Black",
                    "price": 29.99,
                    "isInFavorites": true,
                    "badges": [
                        {
                            "type": "tag",
                            "value": "Sostenibilità"
                        }
                    ]
                }
            ]
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
            <CardApp v-for="product in products" :name="product.name" :brand="product.brand">
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