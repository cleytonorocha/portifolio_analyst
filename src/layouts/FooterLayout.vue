<template>
    <div class="row d-flex text-center pt-5 pb-0">
        <div class="col-12 d-flex align-items-center justify-content-center mb-4">
            <a v-for="(link, index) in links" :key="index" :href="link.href" target="_blank">
                <i :class="link.icon"></i>
            </a>
        </div> 
        <p>&copy; 2023 cleytonorocha. All rights reserved.</p>
    </div>
</template>

<script>
export default {
    name: "FooterLayout",
    data() {
        return {
            links: [
                { href: "https://wa.me/5531996709760?text=I%20saw%20your%20portfolio%20and%20would%20like%20to%20discuss%20further.", icon: "fab fa-whatsapp" },
                { href: "mailto:dev@cleytonorocha.com.br", icon: "fas fa-envelope" },
                { href: "https://t.me/cleytonorocha?start", icon: "fab fa-telegram" }
            ]
        }
    }
}
</script>

<style scoped>
    i {
        font-size: 2rem;
        color: #21243D;
    }
    a {
        margin: 0 12px;
    }
</style>