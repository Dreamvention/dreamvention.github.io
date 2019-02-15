<template>
    <div class="py-4 px-3">
        <v-card>
            <v-img :src="product_thumb.src" height="200px" >
                <v-container
                        fill-height
                        fluid
                        pa-2
                >
                    <v-layout fill-height>
                        <v-flex xs12 align-end flexbox>
                            <span class="headline white--text"></span>
                        </v-flex>
                    </v-layout>
                </v-container>
            </v-img>

            <v-slide-y-transition>
                <v-card-text>
                    <h2>{{product_thumb.title}}</h2>
                    I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.
                </v-card-text>
            </v-slide-y-transition>

            <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn icon>
                    <v-icon>favorite</v-icon>
                </v-btn>
                <a :href="product_thumb.git_link" target="_blank"><v-btn icon>
                    <v-icon>fab fa-git</v-icon>
                </v-btn></a>
            </v-card-actions>
        </v-card>
    </div>
</template>

<script>
	export default {
		name: "ProductThumb",
    props: ['product_thumb'],
	};
</script>

<style scoped>

</style>