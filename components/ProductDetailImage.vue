<template>
    <div>
        <v-img :src="icon_thumb.image">
        </v-img>
    </div>
</template>

<script>
	export default {
		name: "ProductDetailImage",
		props: ['icon_thumb'],
	};
</script>

<style scoped>

</style>