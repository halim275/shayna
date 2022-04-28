<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderShayna from "@/components/HeaderShayna.vue";
import HeroShayna from "@/components/HeroShayna.vue";
import WomanShayna from "@/components/WomanShayna.vue";
import InstaShayna from "@/components/InstaShayna.vue";
import LogoShayna from "@/components/LogoShayna.vue";
import FooterShayna from "@/components/FooterShayna.vue";

export default {
    name: "HomeView",
    components: {
        // HelloWorld
        HeaderShayna,
        HeroShayna,
        WomanShayna,
        InstaShayna,
        LogoShayna,
        FooterShayna,
    },
};
</script>

<template>
    <div class="home">
        <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
        <HeaderShayna />
        <HeroShayna />
        <WomanShayna />
        <InstaShayna />
        <LogoShayna />
        <FooterShayna />
    </div>
</template>
