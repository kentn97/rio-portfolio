<template>
  <div class="top">
    <div class="top__head-wrap">
      <h1 class="top__heading">RIO</h1>
      <SnsList class="top__sns" />
    </div>
    <h2 class="top__desc"><em>"伝わる"</em>イラストを最大限表現します</h2>
    <div class="top__cards">
      <LinkCard link-to="works" />
      <LinkCard link-to="order" />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" scoped>
.top {
  padding: 6rem 12rem;

  &__head-wrap {
    display: flex;
    justify-content: flex-start;
    align-items: center;
  }

  &__heading {
    margin-top: -2rem;

    font-family: 'Sansita', sans-serif;
    font-size: 8.5rem;
    letter-spacing: 0.18em;
    line-height: 1;
  }

  &__sns {
    margin-left: 5rem;
  }

  &__desc {
    margin-top: 6rem;

    font-size: 2.8rem;
    font-weight: 700;

    & em {
      font-size: 3.6rem;
      font-style: normal;
    }
  }

  &__cards {
    display: grid;
    grid-template-columns: repeat(2, max-content);
    justify-content: center;
    column-gap: 6rem;

    margin-top: 12rem;
  }
}
</style>
