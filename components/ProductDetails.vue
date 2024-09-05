<template lang='pug'>
.container
  .card
    .card__img.rel
      .imgs
        img(:src="`${product.image}`")
    h2 {{ product.title }}
    p Prise: {{ product.price }} &euro;
    h3 Product description:
    p {{ product.description }}
  NuxtLink(:to="`/products`" class='linkTo') Back to products
</template>

<script setup>
const { product } = defineProps(['product'])

</script>

<style lang="scss" scoped>
.card {
  display: grid;
  grid-template-columns: 400px 1fr;
  column-gap: 25px;
  height: 100%;
  border-radius: 0.375rem;
  background-color: rgb(255 255 255);
  padding: 0.75rem;
  box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);

  align-content: start;
  row-gap: 15px;

  &__img {
    grid-row: 1/7;
    min-height: 531px;
  }

  h2 {
    font-family: 'MuseoSansCyrl-300', sans-serif;
    font-weight: 300;
    text-transform: none;
    font-size: 22px;
  }

  p {
    &:first-of-type {
      font-family: 'MuseoSansCyrl-300', sans-serif;

    }

  }
}

.linkTo {
  font-family: 'HouschkaPro-DemiBold', sans-serif;
  color: $red-9;
  margin: 20px 0 0 0;
}
</style>