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
    name: "SideBar",
    data() {
        return {
            links: [
                { href: "https://wa.me/yourphonenumber", icon: "fab fa-whatsapp" },
                { href: "mailto:youremail@example.com", icon: "fas fa-envelope" },
                { href: "https://t.me/yourusername", icon: "fab fa-telegram" }
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