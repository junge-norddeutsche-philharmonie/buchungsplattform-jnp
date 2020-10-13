<template>
  <v-app light id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      app
      class="pt-4"
      color="#ed6b6f"
    >

      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">
            Buchung
          </v-list-item-title>
          <v-list-item-subtitle>
            junge norddeutsche philharmonie
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list
        nav
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          :to="item.to"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

    </v-navigation-drawer>

    <v-main>
      <nuxt />
    </v-main>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: true,
      fixed: false,
      items: [
        {
          icon: 'mdi-home',
          title: 'Homepage jnp',
          to: 'https://junge-norddeutsche.de/'
        },
        {
          icon: 'mdi-apps',
          title: 'Übersicht',
          to: '/'
        },
        {
          icon: 'mdi-numeric-1-box-outline',
          title: '1to1 - Hamburg',
          to: '/1to1hamburg'
        },
        {
          icon: 'mdi-numeric-1-box-outline',
          title: '1to1 - Hannover',
          to: '/1to1hannover'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
