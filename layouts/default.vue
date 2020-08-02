<template>
  <div class="page-container" :class="$route.path === '/' && 'bg'">
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

  &.bg {
    background-image: url('~@/assets/imgs/bg-arts.png');
    background-position: right -6.5rem top;
    background-size: auto 100%;
  }
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
