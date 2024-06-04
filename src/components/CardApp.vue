<script>
export default {
    name: 'CardApp',

    props: ['product', 'brand', 'frontImage', 'backImage'],

    data() {
        return {
        }
    },

    methods: {

        findBadgeByType(type) {
            return this.product.badges.find(
                badge => badge.type === type
            )
        },

        discountedPrice(product) {
            let oldPrice = product.price;
            let discount = parseInt(this.findBadgeByType('discount').value.slice(1, 3));
            const newPrice = oldPrice - oldPrice * discount / 100;

            return newPrice.toFixed(2);
        }
    }
}
</script>

<template>
    <div class="col-33">
        <div class="content p-relative">
            <img class="main-image" :src="`../src/assets/img/${product.frontImage}`" alt="">
            <img class="hover-image" :src="`../src/assets/img/${product.backImage}`">

            <div class="labels">
                <span v-if="findBadgeByType('discount')" class="label red-label">{{
                    findBadgeByType('discount').value }}</span>
                <span v-if="findBadgeByType('tag')" class="label green-label">Sostenibilità</span>
            </div>
            <div class="description">
                <div class="brand">{{ product.brand }}</div>
                <div class="clothes-name">{{ product.name }}</div>
            </div>
            <div class="prices">
                <span v-if="findBadgeByType('discount')" class="discount-price">{{ discountedPrice(product) }}&euro;</span>
                <span class="original-price">{{ product.price }}&euro;</span>
            </div>

        </div>
    </div>
</template>