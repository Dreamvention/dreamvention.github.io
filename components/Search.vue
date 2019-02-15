<template>
    <div class="main-div px-3">
        <v-layout row wrap>
            <v-flex>
                <v-toolbar>
                    <v-toolbar-title>{{title}}</v-toolbar-title><v-spacer/>
                    <div style="width: 30%"><v-text-field v-model="searchInput" @input="search"></v-text-field></div>
                    <v-btn icon><v-icon>search</v-icon></v-btn>
                </v-toolbar>
            </v-flex>
        </v-layout>
    </div>
</template>

<script>
	export default {
		name: "Search",
    props: ['title'],
    data() {
			return {
				searchInput: ''
      }
    },
    methods: {
			search() {
          this.$emit('search', {
            search: this.searchInput
          })
      }
    }
	};
</script>

<style scoped>
    .main-div {
        margin-top: 30px;
    }
</style>