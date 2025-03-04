<template>
  <div class="container py-5">
    <div class="row align-items-center justify-content-evenly py-5">
      <!-- Informações de contato -->
      <div class="col-12 col-md-5 mb-4 mb-md-0 text-center">
        <h2 class="contact-item ms-md-5">Get in Touch</h2>
        <div
        v-for="(item, index) in contact"
        :key="index"
        class="contact-item ms-md-5"
        >
          <h5 class="fw-bold">
            <i :class="item.icon"></i> {{ item.type }}
          </h5>
          <p>
            <a :href="item.link" target="_blank" class="contact-link">{{ item.value }}</a>
          </p>
        </div>
      </div>
      <!-- Imagem -->
      <div class="col-12 col-md-6">
        <img
          :src="require(`@/assets/contact.jpg`)"
          alt="Contact Illustration"
          class="img-fluid contact-image"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      contact: [
        {
          type: "Email",
          value: "dev@cleytonorocha.com.br",
          icon: "fas fa-envelope",
          link: "mailto:dev@cleytonorocha.com.br"
        },
        {
          type: "Telegram",
          value: "@cleytonorocha",
          icon: "fab fa-telegram",
          link: "https://t.me/cleytonorocha?start"
        },
        {
          type: "WhatsApp",
          value: "+55 (31) 99670-9760",
          icon: "fab fa-whatsapp",
          link: "https://wa.me/5531996709760?text=I%20saw%20your%20portfolio%20and%20would%20like%20to%20discuss%20further.",
        },
      ],
    };
  },
};
</script>

<style scoped>
.contact-card {
  border-radius: 12px;
}
.contact-image {
  max-width: 100%;
  height: auto;
}
.contact-item {
  margin-bottom: 20px;
}
.contact-item i {
  margin-right: 10px;
}
.contact-link {
  color: #007bff; /* Cor temática */
  text-decoration: none;
}
.contact-link:hover {
  color: #0056b3; /* Cor temática ao passar o mouse */
  text-decoration: underline;
}
</style>