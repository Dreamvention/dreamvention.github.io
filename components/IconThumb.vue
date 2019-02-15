<template>
    <div class="main_div">
        <div class="text-xs-center"><v-icon x-large>{{icon_thumb.icon}}</v-icon></div>
        <Card :icon_thumb="icon_thumb"></Card>
    </div>
</template>

<script>
    import Card from '~/components/Card'

	  export default {
        name: "IconThumb",
        components: {Card},
        props: ['icon_thumb'],
    };
</script>

<style scoped>
    .main_div {
        margin-top: 100px;
        margin-bottom: 140px ;
    }
</style>