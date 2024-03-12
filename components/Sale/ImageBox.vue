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
            <span>Zobacz</span>
          </a>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Image',
    props: {
      link: {
        type: String,
        default: '',
      },
    },
  };
  </script>
  
  <style scoped>

</style>
  