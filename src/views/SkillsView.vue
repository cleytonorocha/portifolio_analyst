<template>
  <section class="pt-5">
    <div class="row container-md px-md-5 mx-md-4 mb-5">
      <h2>Skills</h2>
    </div>
    <div>
      <hr class="d-block d-md-none" />
      <experience-card
        :title="google.title"
        :diretory="google.diretory"
        :images="google.images"
        :textPosition="'right'"
        :heading="google.heading"
        :experience="google.experience"
        :description="google.description"
        data-aos="fade-left" data-aos-duration="1200" 
      />
      <hr class="d-block d-md-none" />
      <experience-card
        :title="office.title"
        :diretory="office.diretory"
        :images="office.images"
        :textPosition="'left'"
        :heading="office.heading"
        :experience="office.experience"
        :description="office.description"
        :icon_size="office.icon_size"
        :disposition="office.disposition"
        data-aos="fade-right" data-aos-duration="1200" 
      />
    </div>
    <hr class="d-block d-md-none" />
    <experience-card
      :title="development.title"
      :diretory="development.diretory"
      :images="development.images"
      :textPosition="'right'"
      :heading="development.heading"
      :experience="development.experience"
      :description="development.description"
      data-aos="fade-left" data-aos-duration="1200" 
    />
  </section>
</template>

<script>
export default {
  name: "SkillsView",

  data() {
    return {
      google: {
        title: "Google",
        diretory: "google",
        images: ["sheets", "docs", "slides", "forms", "drive", "datastudio"],
        heading: "Google Workspace",
        experience: "3 years of experience",
        description:
          "Expert in data management, collaboration, and automation using Google Sheets, Docs, Slides, Forms, and Drive. Proficient in creating complex spreadsheets, documents, presentations, and forms to streamline workflows and enhance productivity.",
      },
      office: {
        title: "Microsoft Office",
        diretory: "microsoft",
        images: ["excel", "word", "powerpoint"],
        heading: "Microsoft Office Suite",
        experience: "3 years of experience",
        description:
          "Expert in data organization, reporting, and automation using Excel, Word, PowerPoint. Skilled in creating detailed reports, professional documents, and engaging presentations to support business operations and decision-making processes.",
        icon_size: "68",
        disposition: "between",
      },
        development: {
            title: "Development",
            diretory: "development",
            images: ["html", "css", "js", "java", "spring", "linux"],
            heading: "Web Development",
            experience: "1 year of experience",
            description:
            "Experience with HTML, CSS, JavaScript, Java, Spring, and Linux. Skilled in building responsive web applications, developing RESTful APIs, and managing server-side operations. Proficient in version control and team collaboration.",
        },
    };
  },

  components: {
    ExperienceCard: () => import("@/components/ExperienceCard.vue"),
  },
};
</script>

<style>
</style>
