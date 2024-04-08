<template>
  <div class="informations">
    <div class="three-box-component">
      <Box v-for="(box, index) in boxes" :key="index">
        <template v-slot:icon>
          <div class="icon" v-if="box.icon !== ''" style="width: 50px; height: 50px;">
            <component :is="box.icon" v-if="typeof box.icon === 'object'" class="svg-icon" />
          </div>
        </template>
        <template v-slot:header>
          <div class="header">{{ box.header }}</div>
        </template>
        <template v-slot:text>
          <div class="text">{{ box.text }}</div>
        </template>
      </Box>
    </div>
  </div>
</template>

<script>
import Box from './Box.vue';
import DiscountSvg from '~/assets/discount.svg'
import DeliverySvg from '~/assets/delivery.svg'
import SecuritySvg from '~/assets/security.svg'

export default {
  components: {
    Box,
  },
  data() {
    return {
      boxes: [
        {
          icon: DiscountSvg,
          header: "skorzystaj z promocji",
          text: "Odwiedzając naszą stronę zawsze możesz liczyć na ciekawe promocje"
        },
        {
          icon: DeliverySvg,
          header: "wysyłka",
          text: "Gwarantujemy wysyłkę w ciągu 24h od zaksięgowania płatności"
        },
        {
          icon: SecuritySvg,
          header: "bezpieczne zakupy",
          text: "Kupując w naszym sklepie masz gwarancję bezpiecznych zakupów i płatności"
        }
      ]
    };
  }
};
</script>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');

.informations {
  background-color: #f9f7f4;
  padding: 80px 0 35px;
  width: 100%;
}

.three-box-component {
  display: flex;
  padding: 20px;
  background-color: rgb(249, 247, 244);
  margin-left: auto;
  margin-right: auto;
  max-width: 1190px;
  flex-wrap: wrap;
  justify-content: space-around;
}

.icon {
  font-size: 24px;
  margin-bottom: 10px;
}

.header {
  color: #000;
  letter-spacing: 1.86px;
  font-weight: 550;
  font-size: 13px;
  line-height: 1.2;
  margin-bottom: 20px;
  text-transform: uppercase;
  font-family: 'Montserrat', sans-serif;
}

.text {
  font-size: 13px;
  font-weight: 400;
  line-height: 1.6;
  margin: 0;
  font-family: 'Montserrat', sans-serif;
}

.svg-icon {
  width: 50px;
  height: 50px; 
}



</style>
