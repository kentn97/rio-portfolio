<template>
  <div class="history-list">
    <HistoryItem
      v-for="(history, index) in historyList"
      :key="index"
      :date="history.date"
      :heading="history.heading"
      :link="history.link && history.link"
      class="history-list__item"
    />
  </div>
</template>

<script lang="ts">
import Vue, { PropType } from 'vue'

interface History {
  date: string
  heading: string
  link?: string
}

export default Vue.extend({
  props: {
    historyList: {
      type: Array as PropType<History[]>,
      required: true,
    },
  },
})
</script>

<style lang="scss" scoped>
.history-list {
  display: grid;
  row-gap: 1rem;

  &__item {
  }
}
</style>
