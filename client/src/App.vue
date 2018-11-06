<template>
  <v-app id="inspire" dark>
    <front-navigation-drawer></front-navigation-drawer>
    <v-toolbar app fixed clipped-left>
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title>Atanas Petrov Foundation</v-toolbar-title>
    </v-toolbar>
    <v-content>
      <v-container fluid fill-height>
        <v-layout justify-center align-center>
          <v-flex shrink>
            <v-tooltip right>
              <v-btn slot="activator" icon large href="https://instagram.com/atanaspetrovfoundation" target="_blank">
                <v-icon large>mdi-codepen</v-icon>
              </v-btn>
              <span>Codepen</span>
            </v-tooltip>
          </v-flex>
          <v-flex id="inspire"><front-page-carousel></front-page-carousel></v-flex>
        </v-layout>
      </v-container>
    </v-content>
    <v-footer app fixed>
      <span>Vienna 2018</span>
    </v-footer>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import FrontPageCarousel from './components/FrontPageCarousel'
import FrontNavigationDrawer from './components/FrontNavigationDrawer'

export default {
  name: 'App',
  components: {
    HelloWorld,
    FrontPageCarousel,
    FrontNavigationDrawer
  },
  data () {
    return {
      clipped: false,
      drawer: true,
      fixed: false,
      items: [{
        icon: 'bubble_chart',
        title: 'Inspire'
      }],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
<style>
#inspire {
  height: 100vh
}
</style>
