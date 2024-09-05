<template lang='pug'>
.container 
  h1 products
  ul
    li(v-for="product in products" :key="index") 
      ProductCard( :product="product")
      
</template>
<script setup>
const { data: products } = await useFetch('https://fakestoreapi.com/products')

</script>
