<script setup>
const props = defineProps(["links", "title"]);

const links = props.links?.links;
</script>

<template>
   <div class="links-box">
      <h3 class="links-box-title">{{ title }}</h3>
      <ul class="links-box-links" v-for="(value, index) in links" :key="index">
         <li class="links-box-link">
            <NuxtLink :to="value.url" class="">{{ value.title }}</NuxtLink>
         </li>
      </ul>
   </div>
</template>

<style scoped lang="scss">
.links-box {
   padding-right: 10px;
   display: flex;
   justify-content: flex-start;
   align-items: flex-start;
   order: 1;
   flex-direction: column;
   text-align: left;
   margin-bottom: 49px;
   flex-basis: 25%;
   flex-grow: 1;
   flex-shrink: 0;
}

.links-box-title {
   font-size: 11px;
   letter-spacing: 0.6px;
   line-height: 1.5;
   font-weight: 700;
   text-transform: uppercase;
   margin-top: 0;
   margin-bottom: 24px;
}

.links-box-links {
   padding: 0;
   margin: 0;
   list-style: none;
}

.links-box-link {
   letter-spacing: 0.3px;
   font-size: 12px;
   line-height: 1.9;
   margin: 0 0 10px;
}

.links-box-link a {
   color: inherit;
}

.links-box-link a:hover {
   color: inherit;
   text-decoration: underline;
}
</style>
