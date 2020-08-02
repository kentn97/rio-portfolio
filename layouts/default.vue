<template>
  <div class="page-container">
    <TheHeader />
    <main>
      <Nuxt />
    </main>
    <TheFooter class="page-footer" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" scoped>
.page-container {
  position: relative;
  width: 114rem;
  margin: 0 auto;

  background-color: #fff;
  box-shadow: 0 2rem 4rem rgba($color-black, 0.08);
}

.page-footer {
  position: fixed;
  top: 60rem;
  left: auto;
  margin-left: 4rem;

  transform-origin: top left;
  transform: rotate(-90deg);
}
</style>
