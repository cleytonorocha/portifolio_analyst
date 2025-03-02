<template>
  <div>
    <nav-bar />
    <section class="container text-center text-md-start">
      <apresentation-view-vue />
    </section>
  </div>
</template>

<script>
import NavBar from "@/layouts/NavBar.vue";
import ApresentationViewVue from "./views/ApresentationView.vue";
export default {
  name: "App",

  components: {
    NavBar,
    ApresentationViewVue,
  },
};
</script>

<style>
* {
  font-family: "Hebbo", sans-serif;
}
section {
  padding: 80px 0;
}
</style>
