<template>
    <a :href="project.projectLink" target="_blank" class="text-decoration-none py-4">
      <div class="card border-0 shadow-sm p-4 d-flex flex-lg-row flex-column align-items-center w-100">
        <div class="col-lg-5 col-12">
          <img
            :src="require(`@/assets/projects/${project.imageSrc}.png`)"
            alt="Project Preview"
            class="img-fluid rounded project-image"
          />
        </div>
        <div class="col-lg-7 col-12 mt-lg-0 mt-3 px-4">
          <h2 class="fw-bold text-dark fs-3">{{ project.title }}</h2>
          <div class="mb-3">
            <span class="badge fs-5 px-3 py-2 me-3">{{ project.year }}</span>
            <span class="text-muted fs-4">{{ project.category }}</span>
          </div>
          <p class="mt-3 text-secondary text-start fs-5">{{ project.description }}</p>
        </div>
      </div>
    </a>
  </template>
  
  <script>
  export default {
    props: {
      project: {
        type: Object,
        required: true,
      },
    },
  };
  </script>
  
  <style scoped>
  .project-image {
    width: 100%;
    height: 300px;
    object-fit: cover;
  }

  .badge {
    background-color: #07218a;
  }
  .card {
    transition: transform 0.2s ease-in-out;
  }
  .card:hover {
    transform: scale(1.02);
  }
  </style>
  