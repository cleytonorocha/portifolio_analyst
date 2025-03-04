<template>
    <section class="pt-5">
        <div class="row container-md px-md-5 mx-md-4 mb-5">
            <h2>Featured Works</h2>
            <project-card
                v-for="(project, index) in projects"
                :key="index"
                :project="project"
                :imagem="project.imageSrc"
                data-aos="fade-right" data-aos-duration="1200"
            />
        </div>
    </section>
</template>

<script>
export default {
    name: "WorkView",

    components: {
        ProjectCard: () => import("@/components/ProjectCard.vue"),
    },

    data() {
        return {
            projects: [
                {
                    title: "Sales Dashboard",
                    year: "2021",
                    category: "Dashboard",
                    description:
                        "A comprehensive sales dashboard providing real-time insights into sales performance, trends, and forecasts.",
                    imageSrc: "img1",
                    projectLink: "https://www.example.com/sales-dashboard",
                },
                {
                    title: "Corporate Website",
                    year: "2021",
                    category: "Website",
                    description:
                        "A modern and responsive corporate website designed to enhance the company's online presence and engagement.",
                    imageSrc: "img2",
                    projectLink: "https://www.example.com/corporate-website",
                },
                {
                    title: "Fitness Tracker App",
                    year: "2021",
                    category: "Mobile App",
                    description:
                        "A mobile application that helps users track their fitness activities, set goals, and monitor progress.",
                    imageSrc: "img3",
                    projectLink: "https://www.example.com/fitness-tracker-app",
                },
                {
                        title: "Financial Analysis Sheets",
                        year: "2021",
                        category: "Sheets",
                        description:
                                "A set of financial analysis sheets to help businesses track and analyze their financial performance.",
                        imageSrc: "img4",
                        projectLink: "https://www.example.com/financial-analysis-sheets",
                }
            ],
        };
    },
};
</script>

<style>
</style>
