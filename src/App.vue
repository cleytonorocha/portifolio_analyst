<template>
  <v-app>
    <NavBar />
    <v-main>
      <v-container>
        <router-view />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import NavBar from "@/layouts/NavBar.vue";

export default {
  name: "App",

  components: {
    NavBar,
  },

};
</script>
