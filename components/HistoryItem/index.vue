<template>
  <div class="history-item">
    <p class="history-item__date">{{ date }}</p>
    <a v-if="link" :href="link" target="_blank" class="history-item__link">{{
      heading
    }}</a>
    <p v-else class="history-item__heading">{{ heading }}</p>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    date: {
      type: String,
      required: true,
    },
    heading: {
      type: String,
      required: true,
    },
    link: {
      type: String,
      default: '',
    },
  },
})
</script>

<style lang="scss" scoped>
.history-item {
  display: grid;
  grid-template-columns: max-content 1fr;
  align-items: start;
  column-gap: 1rem;

  &__date {
    margin-top: 0.25rem;

    color: $color-black-light;
    font-size: 1.4rem;
  }

  &__link,
  &__heading {
    display: inline-block;
    font-weight: 500;
  }

  &__link {
    text-decoration: underline;
    transition: color 0.2s;

    &:hover,
    &:focus {
      color: $color-black-light;
    }
  }
}
</style>
