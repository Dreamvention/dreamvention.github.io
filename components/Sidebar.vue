<template>
    <div class="main-div">
        <v-list>
            <v-list-tile
                v-for="(page, key) of pages"
                :key="key"
                :to="page.to">
                <v-list-tile-action>
                    <v-icon>{{page.icon}}</v-icon>
                </v-list-tile-action>
                <v-list-tile-content>
                    <v-list-tile-title>{{page.title}}</v-list-tile-title>
                </v-list-tile-content>
            </v-list-tile>
        </v-list>
    </div>
</template>

<script>
	export default {
		data() {
			return {
				pages: [
					{
						title: 'Home',
						icon: 'home',
						to: { name: 'index' }
					},
					{
						title: 'Modules',
						icon: 'device_hub',
						to: { name: 'modules' }
					},
					{
						title: 'Development Tools',
						icon: 'desktop_mac',
						to: { name: 'tools' }
					},
					{
						title: 'Online Services',
						icon: 'router',
						to: { name: 'services' }
					},
				]
			}
		}
	}
</script>

<style>
    .main-div {

    }
</style>