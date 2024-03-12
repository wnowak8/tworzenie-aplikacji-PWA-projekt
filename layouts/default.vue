<template>
   <slot />
   <!-- <Content />
   <Sale/> -->
   <Footer />
</template>


<script>
import Content from '~/components/Informations/Content.vue';
import Sale from '~/components/Sale/Sale.vue';

export default {
  components: {
    Content,
    Sale,
  },
};
</script>

