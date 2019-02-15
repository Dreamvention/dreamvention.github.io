<template >
    <div class="mt-5">
        <v-card>
            <v-img
                    class="white--text"
                    height="200px"
                    src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
            >
                <v-container fill-height fluid>
                    <v-layout fill-height>
                        <v-flex xs12 align-end flexbox>
                            <span class="headline">Top 10 Australian beaches</span>
                        </v-flex>
                    </v-layout>
                </v-container>
            </v-img>
            <v-card-title>
                <div>
                    <span class="grey--text">Number 10</span><br>
                    <span>Whitehaven Beach</span><br>
                    <span>Whitsunday Island, Whitsunday Islands</span>
                </div>
            </v-card-title>
            <div class="text-xs-right by_dream_text">
                <em><small>&mdash; Dreamvention</small></em>
            </div>
        </v-card>
    </div>
</template>

<script>
	  export default {
        name: "Hero"
	  };
</script>

<style scoped>
    .main_div {
        margin-top: 20px;
    }
    .by_dream_text {
        margin: 0 20px 0 0;
        padding-bottom: 10px;
    }
</style>