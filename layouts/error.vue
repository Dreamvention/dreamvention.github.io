<template>
        <v-layout justify-center align-center>
            <v-flex xs12 md6 class="text-xs-center mt-5">
                <h1 class="blue--text display-1">Whoops, 404</h1>
                <h3 class="subheading">The page you were looking for does not exist</h3>
                <v-btn class="blue blue--text mt-3" outline :to="{name: 'index'}">Get me out of here</v-btn>
            </v-flex>
        </v-layout>
</template>

<script>
	export default {
		name: "error"
	};
</script>

<style scoped>

</style>