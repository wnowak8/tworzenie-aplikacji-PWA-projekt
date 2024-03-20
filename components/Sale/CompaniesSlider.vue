<template>
  <section class="companies">
    <div class="companies-wrapper">
      <vueper-slides
        class="no-shadow"
        :visible-slides="computedVisibleSlides"
        slide-multiple="computedSlideMultiple"
        :gap="5"
        :slide-ratio="computedSlideRatio"
        :dragging-distance="200"
        :breakpoints="{ 800: { visibleSlides: 3 } }"

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
          link: "",
          altText: "Made in poland",
        },
        {
          imgSrc:
            "https://clickfashion.pl/media/idea07_contenttypes/contenttypeentity/image/2/_/2.png",
          link: "",
          altText: "Naturalne materiały",
        },
        {
          imgSrc:
            "https://clickfashion.pl/media/idea07_contenttypes/contenttypeentity/image/3/_/3.png",
          link: "",
          altText: "Hand Made",
        },
        {
          imgSrc:
            "https://clickfashion.pl/media/idea07_contenttypes/contenttypeentity/image/4/_/4.png",
          link: "",
          altText: "oryginalnosc",
        },
        // Add more company objects as needed
      ],
    };
  },
  computed: {
    computedVisibleSlides() {
      return Math.min(this.companies.length, 4);
    },
    computedSlideRatio() {
      return this.companies.length === 3 ? 1 / 4 : 1 / 8;
    },
    computedSlideMultiple() {
      return this.companies.length > 3 ? 1 : this.companies.length;
    },
  },
  mounted() {
    // Ukryj kropki paginacji
    const paginationDots = document.querySelectorAll('.vueper-pagination');
    paginationDots.forEach(dot => dot.style.display = 'none');
  }
};
</script>
<style>
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
  height: 100%;
}
.company-image {
  padding: 10px;
  margin: auto;


}
.vueperslide__content-wrapper{
  max-width: 188px;
  width: 100%;
  height: auto;
  transition: all .2s ease-in-out;
  padding: 10px;
  
}
.vueperslides__bullets {
  display: none !important;
}
.vueperslides__arrow--next, .vueperslides__arrow--prev {

  color: rgba(0, 0, 0, .2);
  font-size: 8px;
  font-weight: bold;
}


</style>
