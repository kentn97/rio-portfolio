<template>
  <div class="base-heading-1">
    <h1 class="base-heading-1__en">{{ enHeading }}</h1>
    <p class="base-heading-1__jp">{{ jpHeading }}</p>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    enHeading: {
      type: String,
      required: true,
    },
    jpHeading: {
      type: String,
      required: true,
    },
  },
})
</script>

<style lang="scss" scoped>
.base-heading-1 {
  &__en {
    font-family: 'Sansita', sans-serif;
    font-size: 4.2rem;
    font-weight: 800;
    letter-spacing: 0.18em;
  }

  &__jp {
    margin-top: 0.3rem;

    font-size: 2.4rem;
    font-weight: 300;
  }
}
</style>
