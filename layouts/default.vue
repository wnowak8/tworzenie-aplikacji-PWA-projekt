<template>
  <slot />
  <Content />
  <Banner />
  <Sale />
  <CompaniesSlider />
  <Newsletter />
  <Footer />
</template>

<script>
import Content from "~/components/Informations/Content.vue";
import Banner from "~/components/Banner/Banner.vue";
import Sale from "~/components/Sale/Sale.vue";
import CompaniesSlider from "~/components/Sale/CompaniesSlider.vue";

export default {
  components: {
    Content,
    Banner,
    Sale,
    CompaniesSlider,
  },
};
</script>
