<template>
  <div class="product">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <HeaderShayna />

    <FooterShayna />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderShayna from "@/components/HeaderShayna.vue";

import FooterShayna from "@/components/FooterShayna.vue";

export default {
  name: "HomeView",
  components: {
    // HelloWorld
    HeaderShayna,

    FooterShayna,
  },
};
</script>
