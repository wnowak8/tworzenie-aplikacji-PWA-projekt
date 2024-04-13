<template>
  <section class="companies">
    <div class="companies-wrapper" style="margin-left: 150px;">
      <vueper-slides
        ref="slides"
        class="no-shadow"
        :visible-slides="visibleSlides"
        slide-multiple
        :gap="5"
        :slide-ratio="1 / 8"
        :infinite="true"
        :bullets="false"
        :touchable="false"
        :arrows="true"
        :dragging-distance="200"
        :breakpoints="{
          1000: {
            arrows: true,
            infinite: true,
            visibleSlides: 3,
            slideMultiple: 3,
          },
          768: {
            arrows: true,
            infinite: true,
            visibleSlides: 2,
            slideMultiple: 2,
          },
        }"
      >
        <vueper-slide
          v-for="(company, index) in companies"
          :key="index"
          :alt="company.altText"
          :image="company.imgSrc"
        >
          <a :href="company.link">
            <div class="company-container">
              <img :src="company.imgSrc" :alt="company.altText" />
            </div>
          </a>
          <template v-slot:image> </template>
        </vueper-slide>
      </vueper-slides>
    </div>
  </section>
</template>

<script>
import { VueperSlides, VueperSlide } from "vueperslides";
import "vueperslides/dist/vueperslides.css";

export default {
  components: {
    VueperSlides,
    VueperSlide,
  },
  data() {
    return {
      companies: [
        {
          imgSrc:
            "https://clickfashion.pl/media/idea07_contenttypes/contenttypeentity/image/m/a/made_in_poland.png",
          link: "https://clickfashion.pl/",
          altText: "Made in poland",
        },
        {
          imgSrc:
            "https://clickfashion.pl/media/idea07_contenttypes/contenttypeentity/image/2/_/2.png",
          link: "https://clickfashion.pl/",
          altText: "Naturalne materiały",
        },
        {
          imgSrc:
            "https://clickfashion.pl/media/idea07_contenttypes/contenttypeentity/image/3/_/3.png",
          link: "https://clickfashion.pl/",
          altText: "Hand Made",
        },
        {
          imgSrc:
            "https://clickfashion.pl/media/idea07_contenttypes/contenttypeentity/image/4/_/4.png",
          link: "https://clickfashion.pl/",
          altText: "oryginalnosc",
        },
      ],
      visibleSlides: 4,
    };
  },
};
</script>
<style scoped lang="scss">
@media (min-width: 768px) {
  .companies {
    padding: 41px 0 73px;
  }
}

.companies {
  padding: 41px 0 75px;
}
.companies-wrapper {
  margin-left: auto;
  margin-right: auto;
  max-width: 1190px;
  padding-left: 40px;
  padding-right: 40px;
}
.company-container {
  width: 100%;
  height: auto;
  display: flex;
  justify-content: center;
}

.vueperslide:nth-child(1),
.vueperslide:nth-child(3),
.vueperslide:nth-child(4) {
  background-size: auto;
  background-repeat: no-repeat;
  max-width: 188px;
  transition: transform 0.2s ease-in-out;
}
.vueperslide:nth-child(1):hover,
.vueperslide:nth-child(3):hover,
.vueperslide:nth-child(4):hover {
  transform: scale(1.2);
}
.vueperslide:nth-child(2) {
  max-width: 188px;
  max-height: 130px;
  background-size: cover;
  transition: transform 0.2s ease-in-out;
}
.vueperslide:nth-child(2):hover {
  transform: scale(1.2);
}
.vueperslides__bullets {
  display: none !important;
}
.vueperslides__arrow--next,
.vueperslides__arrow--prev {
  color: rgba(0, 0, 0, 0.2);
  font-size: 8px;
  font-weight: bold;
}
.vueperslides__track-inner {
  justify-content: center;
}
@media (max-width: 768px) {
  .vueperslides__track-inner {
    justify-content: flex-start;
  }
}
</style>
