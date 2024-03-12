<template>
  <div class="sale">
  <span class="section-title">Promocje</span>
    <div>
      <Image :link="outlet.link">
        <template v-slot:image>
          <img loading="lazy" :src="outlet.imageSrc" :alt="outlet.alt" />
        </template>
        <template v-slot:text>{{ outlet.text }}</template>
        <template v-slot:description>{{ outlet.description }}</template>
      </Image>
  
      <Image :link="collection.link">
        <template v-slot:image>
          <img loading="lazy" :src="collection.imageSrc" :alt="collection.alt" />
        </template>
        <template v-slot:text>{{ collection.text }}</template>
        <template v-slot:description>{{ collection.description }}</template>
      </Image>
    </div>
  </div>
  </template>
  
  <script>
  import Image from '~/components/Sale/ImageBox.vue';
  
  export default {
    components: {
      Image,
    },
    data() {
      return {
        outlet: {
          link: 'https://clickfashion.pl/',
          imageSrc: 'https://clickfashion.pl/media/idea07_contenttypes/contenttypeentity/image/1/_/1_1.png',
          alt: 'Wyprzedaż 2023',
          text: 'Outlet',
          description: 'Wyprzedaż 2023',

        },
        collection: {
          link: 'https://clickfashion.pl/',
          imageSrc: 'https://clickfashion.pl/media/idea07_contenttypes/contenttypeentity/image/w/y/wyprzeda_.png',
          alt: 'Nowa kolekcja',
          text: 'Kolekcja 2020',
          description: 'Nowa kolekcja',

        },
      };
    },
  };
  </script>
  
  <style scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');

.sale {
  text-align: center;
  flex-wrap: wrap;
}

.section-title {
  font-family: 'Montserrat', sans-serif;
  font-size: 2.8rem;
  font-weight: 700;
  line-height: 1.2;
  color: #000;
  letter-spacing: 1.2px;
  margin-bottom: 20px;
}

.image-container {
  display: flex;
  justify-content: space-around;
  margin: 0 auto;

}
.image-box img {
  max-width: 500px;
  height: auto; 
}
  </style>
  