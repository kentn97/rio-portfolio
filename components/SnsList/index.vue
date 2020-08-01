<template>
  <div class="sns-list">
    <SnsBlock sns="twitter" class="sns-list__item" />
    <SnsBlock sns="instagram" class="sns-list__item" />
    <SnsBlock sns="email" class="sns-list__item" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" scoped>
.sns-list {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1rem;

  width: 31rem;

  &__item {
    &:last-child {
      grid-column: 1 / -1;
    }
  }
}
</style>
