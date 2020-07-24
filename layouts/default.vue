<template>
  <div class="page-container">
    <TheHeader />
    <Nuxt />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" scoped>
.page-container {
  width: 114rem;
  margin: 3rem auto;

  background-color: #fff;
  box-shadow: 0 2rem 4rem rgba($color-black, 0.08);
}
</style>
