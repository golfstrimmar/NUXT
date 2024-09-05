<template lang='pug'>
.container 
  h1 users 
  ul
    li(v-for="user in users" :key="index") 
      NuxtLink(:to="`/users/${user}`") link to User {{ user }}
</template>
<script setup>
const users = [
  1, 2, 3, 4, 5
];

</script>
