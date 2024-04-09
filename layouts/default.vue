<template>
   <slot />
   <Header />
   <Content />
   <Sale />
   <CompaniesSlider />
   <Newsletter />
   <Footer />
</template>

<script>
import Content from '~/components/Informations/Content.vue';
import Sale from '~/components/Sale/Sale.vue';
import CompaniesSlider from '~/components/Sale/CompaniesSlider.vue';
import Header from '~/components/Header/Header.vue'


export default {
  components: {
    Content,
    Sale,
    CompaniesSlider,
    Header
  },
};
</script>
