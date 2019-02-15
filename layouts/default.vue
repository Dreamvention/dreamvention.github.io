<template>
  <div>
    <v-app id="inspire">
      <v-navigation-drawer
              v-model="drawer"
              fixed
              app
      >
        <Sidebar/>
      </v-navigation-drawer>
      <v-toolbar color="light-blue lighten-2" dark fixed app>
        <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
        <v-toolbar-title>Dreamvention</v-toolbar-title>
      </v-toolbar>
      <v-content>
        <v-container fluid fill-height>
          <nuxt/>
        </v-container>
        <Footer></Footer>
      </v-content>
    </v-app>
  </div>
</template>

<script>
  import Sidebar from '~/components/Sidebar';
  import Footer from '~/components/Footer';

  export default {
    components: {Sidebar, Footer},
    data: () => ({
      drawer: false,
    }),
  }
</script>