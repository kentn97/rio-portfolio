<template>
  <h3 class="base-heading-2">
    <slot />
  </h3>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" scoped>
.base-heading-2 {
  display: inline-block;
  padding: 0 0.6rem;

  font-size: 1.8rem;
  font-weight: 700;

  background: linear-gradient(transparent 60%, rgba($color-green, 0.6) 60%);
}
</style>
