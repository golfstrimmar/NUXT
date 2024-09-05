<template lang='pug'>
.card
  img(:src="`${product.image}`")
  p {{product.title}}
  NuxtLink(:to="`/products/${product.id}`") View Details
</template>


<script setup>
const { product } = defineProps(['product'])
</script>

<style scoped>
.thumb {
  max-height: 120px;
  max-width: 70%;
  margin: 0 auto;
}
</style>