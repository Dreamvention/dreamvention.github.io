<template>
    <v-footer dark height="auto">
        <v-card class="flex" flat tile>
            <v-card-title class="light-blue lighten-2">
                <v-layout row wrap>
                    <v-flex xs12 sm8 md8 lg8>
                        <div class="ml-2" style="padding-top: 11px"><strong class="subheading">Get connected with us on social networks!</strong></div>
                    </v-flex>
                    <v-flex class="text-md-right">
                        <div class="mr-4">
                            <a v-for="icon in icons" :key="icon.icon" :href="icon.link" target="_blank">
                                <v-btn
                                        class="mx-3"
                                        dark
                                        icon
                                >
                                    <v-icon size="24px">{{ icon.icon }}</v-icon>
                                </v-btn>
                            </a>
                        </div>
                    </v-flex>
                </v-layout>

            </v-card-title>

            <v-card-actions class="grey darken-3 justify-center pa-3">
                &copy; {{getYear()}} — <strong style="margin-left: 5px">Dreamvention</strong>
            </v-card-actions>
        </v-card>
    </v-footer>
</template>

<script>
	export default {
		data() {
			return {
		    icons: [
            {icon: 'fab fa-facebook', link: 'https://www.facebook.com/dreamvention'},
            {icon: 'fab fa-instagram', link: ''},
            {icon: 'fab fa-youtube', link: 'https://www.youtube.com/channel/UCZ5duyrL4sfii1pqvQqQYlg'}
          ]
      }
		},
    methods: {
			  getYear: function () {
            let date = new Date();
            return date.getFullYear();
			  }
    }
	}
</script>

<style>
    a {
        text-decoration: none;
    }
    a:hover {
        text-decoration: none;
    }
</style>