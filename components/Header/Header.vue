<template>
  <header>
    <div class="user-panel">
      <img src="~/assets/logo.png" alt="logo" />
      <UserMenu />
    </div>
    <Nav />
  </header>
</template>

<script setup>
import Nav from "~/components/Header/Nav.vue";
import UserMenu from "~/components/Header/UserMenu.vue";
</script>

<style scoped lang="scss">
header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.user-panel {
  display: flex;
  padding: 25px 40px;
  width: 100%;
  max-width: 1600px;
  justify-content: space-between;
  align-items: center;

  @media screen and (max-width: 1700px) {
    max-width: 1140px;
  }
}
</style>
