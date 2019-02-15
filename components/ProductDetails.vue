<template>
    <div class="main_div">
        <v-layout align-start justify-space-between wrap>
            <v-flex xs12 sm6 md5 class="one-content-div">
                <div v-if="position === 'left'" class="image-div"><ProductDetailImage :icon_thumb="icon_thumb"></ProductDetailImage></div>
                <div v-else class="text-div"><ProductDetailText :icon_thumb="icon_thumb"></ProductDetailText></div>
            </v-flex>
            <v-flex xs12 sm6 md5>
                <div v-if="position === 'left'"  class="text-div"><ProductDetailText :icon_thumb="icon_thumb"></ProductDetailText></div>
                <div v-else  class="image-div"><ProductDetailImage :icon_thumb="icon_thumb"></ProductDetailImage></div>
            </v-flex>
        </v-layout>
    </div>
</template>

<script>

    import ProductDetailText from '~/components/ProductDetailText';
    import ProductDetailImage from '~/components/ProductDetailImage';

export default {
    name: "ProductDetails",
    components: {ProductDetailText, ProductDetailImage},
    props: ['position', 'icon_thumb'],
};
</script>

<style scoped >
    .main_div {
        margin-bottom: 80px;
    }
    .image-div {

    }
    .text-div {
        font-size: 20px;
        line-height: 40px;
    }
</style>