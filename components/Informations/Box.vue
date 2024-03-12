<template>
  <div class="box">
    <slot name="icon"></slot>
    <slot name="header"></slot>
    <slot name="text"></slot>
  </div>
</template>

<script>
export default {
  name: 'Box'
};
</script>

<style scoped>
.box {
  flex: 1;
  text-align: center;
  padding: 20px;
  margin: 0 10px;
  background-color: rgb(249, 247, 244);
  border-radius: 8px;
}


</style>
