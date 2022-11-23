<template>

  <v-app>
    <v-app-bar elevation="0" color="white" height="38px" >
      <router-link
        v-for="(link, i) in links"
        :key="i"
        :to="link.path"
        class="caption pa-2 black--text"
      >
        {{ link.name }}</router-link
      >
      <v-spacer></v-spacer>
    </v-app-bar>
    <v-main>
      <router-view />
    </v-main>

  <v-footer
    dark
    padless
  >
    <v-card
      class="flex"
      flat
      tile
    >
      <v-card-title class="teal">
        <strong class="subheading">Get connected with us on our social networks!</strong>

        <v-spacer></v-spacer>

        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4"
          dark
          icon
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-title>

      <v-card-text class="py-2 white--text text-center">
      <h2 class="font-weight-medium body-2">realme India</h2>
      </v-card-text>
    </v-card>
  </v-footer>
  </v-app>
</template>


<script>
export default {
  name: "App",
  data() {
    return {
      links: [
        {
          path: "/",
          name: "Home",
        },
        {
          path: "/about",
          name: "About",
        },
        {
          path: "/blog",
          name: "Blog",
        },
        {
          path: "/traning",
          name: "Traning",
        },
        {
          path: "/event",
          name: "Event",
        },
        {
          path: "/shop",
          name: "Shop",
        },
        {
          path: "/contact",
          name: "Contact",
        },
      ],
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    };
  },
};
</script>

<style>
a {
  text-decoration: none;
}
</style>
