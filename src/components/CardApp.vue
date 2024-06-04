<script>
export default {
    name: 'CardApp',

    props: ['name', 'brand', 'frontImage', 'backImage'],

    data() {
        return {

        }
    }

}
</script>

<template>
    <div class="col-33">
        <div class="content p-relative">
            <img class="main-image" :src="`../src/assets/img/${frontImage}`" alt="">
            <img class="hover-image" :src="`../src/assets/img/${backImage}`">

            <div class="labels">
                <span class="label red-label">-50%</span>
                <span class="label green-label">Sostenibilità</span>
            </div>
            <div class="description">
                <div class="brand">{{ brand }}</div>
                <div class="clothes-name">{{ name }}</div>
            </div>
            <div class="prices">
                <span class="discount-price">14,99&euro;</span>
                <span class="original-price">29,99&euro;</span>
            </div>

        </div>
    </div>
</template>