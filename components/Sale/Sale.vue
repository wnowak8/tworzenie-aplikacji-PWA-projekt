<template>
  <div class="sale">
    <span class="section-title">Promocje</span>
    <Image :link="outlet.link">
      <template v-slot:image>
        <img loading="lazy" :src="outlet.imageSrc" :alt="outlet.alt" />
      </template>
      <template v-slot:text>
        <p class="text">{{ outlet.text }}</p>
      </template>
      <template v-slot:description>
        <p class="description">{{ outlet.description }}</p>
      </template>
    </Image>

    <Image :link="collection.link">
      <template v-slot:image>
        <img loading="lazy" :src="collection.imageSrc" :alt="collection.alt" />
      </template>
      <template v-slot:text>
        <p class="text">{{ collection.text }}</p>
      </template>
      <template v-slot:description>
        <p class="description">{{ collection.description }}</p>
      </template>
    </Image>
  </div>
</template>

<script>
import Image from "~/components/Sale/ImageBox.vue";

export default {
  components: {
    Image,
  },
  data() {
    return {
      outlet: {
        link: "https://clickfashion.pl/",
        imageSrc:
          "https://clickfashion.pl/media/idea07_contenttypes/contenttypeentity/image/1/_/1_1.png",
        alt: "Wyprzedaż 2023",
        text: "Outlet",
        description: "Wyprzedaż 2023",
      },
      collection: {
        link: "https://clickfashion.pl/",
        imageSrc:
          "https://clickfashion.pl/media/idea07_contenttypes/contenttypeentity/image/w/y/wyprzeda_.png",
        alt: "Nowa kolekcja",
        text: "Kolekcja 2020",
        description: "Nowa kolekcja",
      },
    };
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap");


@media (min-width: 1200px) {
  .sale {
    padding: 0 10px;
  }
}

@media (min-width: 768px) {
  .sale {
    justify-content: space-between;
    padding: 0 40px;
  }
}
.sale {
  display: flex;
  flex-wrap: wrap;
  padding: 0 15px;
  max-width: 1440px;
  width: 100%;
  margin: 0 auto 17px;
}

.section-title {
  font-family: "Montserrat", sans-serif;
  font-size: 36px;
  font-weight: 700;
  flex: 1 0 100%;
  line-height: 1.2;
  color: #000;
  letter-spacing: 1.2px;
  margin-bottom: 20px;
  padding-top: 61px;
  text-align: center;
  border-top: 1px solid #f5f5f5;
  width: 100%;
}

@media (min-width: 768px) {
  .section-title {
    letter-spacing: 0.6px;
  }
}

@media (min-width: 992px) {
  .section-title {
    margin-bottom: 40px;
  }
}

@media (min-width: 1200px) {
  .section-title {
    margin-bottom: 60px;
  }
}

.image-box img {
  max-width: 100%;
  height: auto;
  border: 0;
}
.description {
  font-family: "Montserrat", sans-serif;
  font-size: 12px;
  color: #000;
  margin-bottom: 0;
}
.text {
  font-family: "Montserrat", sans-serif;
  font-size: 12px;
  color: #fff;
  text-transform: uppercase;
  line-height: 1.2;
  letter-spacing: 2.3px;
  margin-bottom: 12px;
  margin-top: 0;
  font-style: normal;
  font-weight: 400;
}
</style>
