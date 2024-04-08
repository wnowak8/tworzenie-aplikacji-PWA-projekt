<template>
  <div class="user-menu">
    <span class="material-symbols-outlined"> search </span>
    <a href="https://clickfashion.pl/customer/account/"
      ><span class="material-symbols-outlined"> person </span></a
    >
    <a href="https://clickfashion.pl/wishlist/">
      <span class="material-symbols-outlined"> favorite </span>
    </a>
    <div class="separation"></div>
    <a href="https://clickfashion.pl/checkout/cart/">
      <span class="material-symbols-outlined"> shopping_bag </span>
    </a>
  </div>
</template>

<script setup></script>

<style scoped>
.user-menu {
  display: flex;
  align-items: center;
  gap: 20px;
}

.separation {
  display: block;
  width: 2px;
  height: 24px;
  background-color: rgb(216, 216, 216);
}

a {
  color: black;
  text-decoration: none;
}
</style>
