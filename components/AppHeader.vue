<template lang='pug'>
header 
  nav
    ul
      li
        NuxtLink(to='/') Home
      li
        NuxtLink(to='/about') About


</template>
<script setup>
</script>
<style lang='scss' scoped>
header {
  nav {
    box-shadow: 0 1px 5px rgba(0, 0, 0, 0.2), 0 2px 2px rgba(0, 0, 0, 0.14), 0 3px 1px -2px rgba(0, 0, 0, 0.12);
    background: $amber-6;
    color: #fff !important;
    position: relative;
    padding: 0 10px;
    min-height: 50px;
    width: 100%;
    display: flex;
    align-items: center;

    ul {
      display: flex;
      align-items: center;
      flex-wrap: nowrap;

      li {
        a {

          &.router-link-active {}
        }

      }
    }
  }
}
</style>