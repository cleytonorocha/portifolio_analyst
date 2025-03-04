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
          <h5 class="fw-bold"><i :class="item.icon"></i> {{ item.type }}</h5>
          <p>{{ item.value }}</p>
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
        },
        {
          type: "Telegram",
          value: "@exemplo_telegram",
          icon: "fab fa-telegram",
        },
        {
          type: "WhatsApp",
          value: "+55 (11) 98888-8888",
          icon: "fab fa-whatsapp",
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
</style>