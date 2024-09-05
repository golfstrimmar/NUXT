<template lang='pug'>
h1 user : {{ id }}
</template>
<script setup>
const { id } = useRoute().params
</script>
<style lang='scss' scoped></style>
