<template>
  <v-app dark>
    <v-navigation-drawer
      persistent
      :mini-variant="miniVariant"
      :clipped="clipped"
      v-model="drawer"
      app
    >
      <v-list>
        <v-list-tile @click="drawer = !drawer"
          router
          :to="item.to"
          :key="i"
          v-for="(item, i) in items"
          exact
        >
          <v-list-tile-action>
            <v-icon v-html="item.icon"></v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title v-text="item.title"></v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar fixed app :clipped-left="clipped">
      <v-toolbar-side-icon @click="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title v-text="title"></v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>
    <main>
      <v-content>
        <v-container>
          <nuxt />
        </v-container>
      </v-content>
    </main>
    <v-footer :fixed="fixed" app>
      <a href="http://kitebot.ca/">Kitebot</a>
    </v-footer>
  </v-app>
</template>

<script>
  export default {
    data () {
      return {
        clipped: true,
        drawer: false,
        fixed: true,
        items: [
          { icon: 'apps', title: 'Vueler', to: '/' },
          { icon: 'apps', title: 'Frequently Asked Questions', to: '/faq' },
          { icon: 'apps', title: 'Get Started', to: '/start' },
          { icon: 'bubble_chart', title: 'Problem 1', to: '/1' }
        ],
        miniVariant: false,
        title: 'Vueler'
      }
    }
  }
</script>
