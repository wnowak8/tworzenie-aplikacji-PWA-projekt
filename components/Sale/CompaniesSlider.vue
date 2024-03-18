<template>
  <section class="companies">
    <div class="companies-wrapper">
      <div
        class="companies-slider slick-initialized slick-slider"
        id="js-companies-slider"
      >
        <div class="slick-list draggable">
          <div class="slick-track">
            <div
              v-for="(company, index) in companies"
              :key="index"
              class="slick-slide slick-active"
            >
              <div class="companies-slide">
                <a :href="company.link" tabindex="0">
                  <img :src="company.imgSrc" :alt="company.altText" />
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Companies from "./Companie.vue";

export default {
  components: {
    Companies,
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
      ],
    };
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}
@media (min-width: 768px) {
  .companies {
    padding: 41px 0 73px;
  }
}
.companies-wrapper {
  margin-left: auto;
  margin-right: auto;
  max-width: 1190px;
  padding-left: 40px;
  padding-right: 40px;
}
div {
  display: block;
}

.companies-slider.slick-initialized {
  visibility: visible;
  opacity: 1;
}
@media (min-width: 1200px) {
  .companies-slider {
    padding: 0 35px;
  }
}
.slick-slider {
  position: relative;
  display: block;
  box-sizing: border-box;
}
.companies-slider {
  display: flex;
  opacity: 0;
  visibility: hidden;
  transition: opacity 1s ease;
}
.slick-list {
  position: relative;
  overflow: hidden;
  display: block;
  margin: 0;
  padding: 0;
}
.slick-track {
  position: relative;
  left: 0;
  top: 0;
  display: flex;
  height: auto;
  justify-content: center;
  align-items: center;
}
.slick-slide {
  height: 100%;
}

.slick-initialized .slick-slide {
  display: inline-block;
  text-align: center;
  height: auto;
}
.slick-initialized .slick-slide.slick-active {
  height: 100%;
}
.companies .slick-slide {
  padding: 10px;
  height: auto;
  overflow: hidden;
  margin: 0;
  box-sizing: border-box;
  width: calc(25% - 20px);
}
@media (min-width: 768px) {
  .companies .slick-slide {
    width: calc(20% - 25px);
  }
}
.companies .slick-slide img {
  max-width: 100%;
}
.companies-slide {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
}
</style>
