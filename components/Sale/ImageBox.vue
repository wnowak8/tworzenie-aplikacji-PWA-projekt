<template>
  <div class="image-box">
    <slot name="image"></slot>
    <div class="sale-content">
      <p class="sale-text"><slot name="text"></slot></p>
      <div data-content-type="html" data-appearance="default" data-element="main" data-decoded="true">
        <slot name="description"></slot>
      </div>
      <div class="sale-link-btn">
        <a :href="link" title="Zobacz" class="sale-link">
          <span class="button-text">Zobacz</span>
          <ArrowSvg class="arrow-icon"/>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import ArrowSvg from '~/assets/arrow.svg'

export default {
  name: 'Image',
  props: {
    link: {
      type: String,
      default: '',
    },
  },
  components: {
    ArrowSvg,
  },
};
</script>

<style scoped>
.sale-link-btn {
  background-color: black;
  border: 2px solid white;
  display: inline-flex;
  align-items: center; 
  justify-content: center;
  padding: 10px 20px;
  transition: background-color 0.3s, color 0.3s, border-color 0.3s;
}

.sale-link-btn a {
  color: white;
  text-decoration: none;
  text-transform: uppercase;
  font-family: 'Montserrat', sans-serif;
  font-weight: 700;
  letter-spacing: 1.83px;
  font-size: 10px;
  display: flex; 
  align-items: center; 
}

.sale-link-btn:hover {
  background-color: white;
  border-color: black;
}

.sale-link-btn:hover a {
  color: black;
}

.button-text {
  margin-right: 75px; 
}

.arrow-icon {
  width: 20px;
  height: 20px;
  fill: white;
  transition: fill 0.3s, transform 0.3s;
  filter: drop-shadow(0 0 2px rgba(255, 255, 255, 0));

}

.sale-link-btn:hover .arrow-icon {
  fill: black;
  filter: drop-shadow(0 0 2px rgba(0, 0, 0, 0));

}
</style>
