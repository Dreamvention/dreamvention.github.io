<template>
    <v-hover>
        <v-card
                slot-scope="{ hover }"
                :class="`elevation-${hover ? 12 : 2}`"
                class="mx-auto card"
                width="100%">
            <v-img
                    src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
                    height="200px"
            >
            </v-img>

            <v-card-title primary-title>
                <div>
                    <div class="headline">{{icon_thumb.title}}</div>
                    <span class="grey--text">1,000 miles of wonder</span>
                </div>
            </v-card-title>

            <v-card-actions>
                <v-btn flat>Share</v-btn>
                <v-btn flat color="purple">Explore</v-btn>
                <v-spacer></v-spacer>
                <v-btn icon @click="icon_thumb.show = !icon_thumb.show">
                    <v-icon>{{ icon_thumb.show ? 'keyboard_arrow_down' : 'keyboard_arrow_up' }}</v-icon>
                </v-btn>
            </v-card-actions>

            <v-slide-y-transition>
                <v-card-text v-show="icon_thumb.show">
                    I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.
                </v-card-text>
            </v-slide-y-transition>
        </v-card>
    </v-hover>
</template>

<script>
	export default {
		name: "Card",
        props: ['icon_thumb']
	};
</script>

<style scoped>
    .card {
        margin-top: 20px;
    }
</style>