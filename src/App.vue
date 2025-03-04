<template>
  <div>
    <nav-bar />

    <section id="home" class="container text-center text-md-start py-0">
      <apresentation-view-vue
        style="min-height: 100vh"
        data-aos="fade-up"
        data-aos-duration="1000"
      />

      <hr id="skills" />
      <skills-view-vue />

      <hr id="works" />
      <work-view-vue />

      <hr id="contact" />
      <contact-view-vue data-aos="zoom-in" data-aos-duration="1200" />

      <footer-layout data-aos="fade-up" />
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
    WorkViewVue: () => import("@/views/WorkView.vue"),
    ContactViewVue: () => import("@/views/ContactView.vue"),
    FooterLayout: () => import("@/layouts/FooterLayout.vue")
  },
};
</script>

<style>
* {
  font-family: "Hebbo";
  box-sizing: border-box;
}
section {
  padding: 80px 0;
}
</style>
