<template>
  <div class="container my-5">
    <div class="row align-items-center justify-content-around py-5">
      <!-- Icons (Left on Desktop, Top on Mobile) -->
      <div
        :class="textPosition === 'left' ? 'col-md-5 order-md-2' : 'col-md-5'"
        class="d-none d-md-block"
      >
        <div class="p-3 border rounded-5 shadow bg-white icon-container">
          <h5 class="fw-lighter fs-3 m-4 mb-5">{{ title }}</h5>
          <div class="d-flex justify-content-center gap-3 flex-wrap mt-3">
            <template>
              <div class="row mx-auto">
                <div :class="`col-12 d-flex justify-content-${disposition}`">
                  <div
                    v-for="image in images.slice(0, 3)"
                    :key="image"
                    class="col-3 d-flex justify-content-around"
                  >
                    <img
                      :src="require(`@/assets/logos/${diretory}/${image}.svg`)"
                      :width="icon_size"
                    />
                  </div>
                </div>
                <div class="col-12 d-flex justify-content-around ms-4 my-4">
                  <div
                    v-for="image in images.slice(3, 6)"
                    :key="image"
                    class="col-3 d-flex justify-content-center"
                  >
                    <img
                      :src="require(`@/assets/logos/${diretory}/${image}.svg`)"
                      :width="icon_size"
                    />
                  </div>
                </div>
              </div>
            </template>
          </div>
        </div>
      </div>

      <!-- Text (Right on Desktop, Below on Mobile) -->
      <div
        :class="[
          textPosition === 'left' ? 'col-md-5 order-md-1' : 'col-md-5',
          textPosition === 'left' ? 'border-md-end' : 'border-md-start'
        ]"
        class="text-start"
        style="height: 200px;"
      >
        <div
          class="ps-md-4 d-flex flex-column"
          style="height: 100%;"
        >
          <h4 class="fw-bold mb-1 fs-2">{{ heading }}</h4>
          <div class="d-flex justify-content-between text-muted small">
            <span>{{ experience }}</span>
            <div class="d-block d-md-none">
              <span v-for="(image, index) in images" :key="index">
                <img
                  :src="require(`@/assets/logos/${diretory}/${image}.svg`)"
                  width="13"
                  class="me-2"
                />
              </span>
            </div>
          </div>
          <p class="mb-0 my-4">{{ description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ExperienceCard",
  props: {
    title: {
      type: String,
      required: true,
    },
    diretory: {
      type: String,
      required: true,
    },
    images: {
      type: Array,
      required: true,
    },
    textPosition: {
      type: String,
      default: "right",
      validator: (value) => ["left", "right"].includes(value),
    },
    heading: {
      type: String,
      required: true,
    },
    experience: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    icon_size: {
      type: String,
      default: "58",
    },
    disposition: {
      type: String,
      default: "around",
      validator: (value) => ["between", "around"].includes(value),
    },
  },
};
</script>

<style scoped>
.border-md-end {
  border-right: none;
}

.border-md-start {
  border-left: none;
}

@media (min-width: 768px) {
  .border-md-end {
    border-right: 1px solid #dee2e6;
  }

  .border-md-start {
    border-left: 1px solid #dee2e6;
  }
}
</style>