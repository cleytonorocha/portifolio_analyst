<template>
  <div>
    <nav-bar />
    <section class="container text-center text-md-start">
      <apresentation-view-vue />
      <hr>
      <skills-view-vue />
      <hr>
      <work-view-vue />
      <hr>
    </section>
  </div>
</template>

<script>
export default {
  name: "App",

  components: {
    NavBar: () => import("@/layouts/NavBar.vue"),
    ApresentationViewVue: () => import("@/views/ApresentationView.vue"),
    SkillsViewVue: () => import("@/views/SkillsView.vue"),
    WorkViewVue: () => import("@/views/WorkView.vue")
  },
};
</script>

<style>
* {
  font-family: "Hebbo";
}
section {
  padding: 80px 0;
}
</style>
