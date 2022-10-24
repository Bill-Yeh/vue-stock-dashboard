<template>
  <v-card>
    <v-toolbar flat dark rounded="0" extended>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Stock Dashboard</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-logout</v-icon>
      </v-btn>
    </v-toolbar>
    <v-navigation-drawer app v-model="drawer" dark absolute temporary>
      <v-list>
        <v-list-item-group class="d-flex">
          <v-list-item-icon dark class="ml-3 mr-4">
            <v-icon large>mdi-cash-100</v-icon>
          </v-list-item-icon>
          <v-list-item-title class="text-h5">
            Stock Dashboard
          </v-list-item-title>
        </v-list-item-group>
        <v-list-item-group v-model="model" mandatory dark>
          <v-list-item v-for="(item, i) in items" :key="i">
            <v-list-item-icon>
              <v-icon v-text="item.icon"></v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title v-text="item.text"></v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
      <!-- <v-list nav dense>
        <v-list-title>Dashboard</v-list-title>
        <v-list-item-group v-model="group" active-class="white--text">
          <v-list-item>
            <v-list-item-title>Foo</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title>Bar</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title>Fizz</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title>Buzz</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list> -->
    </v-navigation-drawer>
    <!-- <v-app-bar color="deep-purple accent-4" dark prominent>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>My files</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-filter</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar> -->
  </v-card>
</template>

<script>
/* eslint-disable */
  export default {
    data: () => ({
      drawer: false,
      group: null,
      items: [
        {
          icon: 'mdi-wifi',
          text: 'Wifi',
        },
        {
          icon: 'mdi-bluetooth',
          text: 'Bluetooth',
        },
        {
          icon: 'mdi-chart-donut',
          text: 'Data Usage',
        },
      ],
      model: 1,
    }),

    watch: {
      group () {
        this.drawer = false
      },
    },
  }
  /* eslint-disable */
</script>
