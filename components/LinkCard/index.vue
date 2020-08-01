<template>
  <n-link :to="'/' + linkInfo.menu" class="link-card" :class="linkInfo.menu">
    <div class="link-card__main">
      <h3 class="link-card__heading">{{ linkInfo.en_heading }}</h3>
      <p class="link-card__jp-heading">{{ linkInfo.jp_heading }}</p>
      <p class="link-card__desc">
        <span>{{ linkInfo.desc1 }}</span
        ><span>{{ linkInfo.desc2 }}</span>
      </p>
    </div>
    <img
      :src="require(`@/assets/imgs/${linkInfo.img}`)"
      alt=""
      class="link-card__img"
    />
  </n-link>
</template>

<script lang="ts">
import Vue from 'vue'
import { linkCardInfo } from '~/utils/data'

export default Vue.extend({
  props: {
    linkTo: {
      type: String,
      required: true,
    },
  },
  computed: {
    linkInfo() {
      return this.linkTo === 'works' ? linkCardInfo.works : linkCardInfo.order
    },
  },
})
</script>

<style lang="scss" scoped>
.link-card {
  display: flex;
  justify-content: space-between;
  width: 40rem;
  height: 18rem;
  padding: 2rem;

  color: #fff;

  box-shadow: 0 1rem 2rem rgba($color: #000000, $alpha: 0.1);
  transition: filter 0.2s;

  &:hover,
  &:focus {
    filter: brightness(0.95);
  }

  &.works {
    background: linear-gradient(
      125.86deg,
      #91cd81 0%,
      rgba(145, 205, 129, 0.98) 48.44%,
      rgba(217, 247, 208, 0.9) 100%
    );
  }
  &.order {
    background: linear-gradient(
      125.86deg,
      #e3bb83 0%,
      rgba(227, 187, 131, 0.98) 50%,
      rgba(255, 246, 234, 0.9) 100%
    );
  }

  &__main {
    display: grid;
    grid-template-rows: repeat(2, min-content) 1fr;
  }

  &__heading {
    font-family: 'Sansita', sans-serif;
    font-size: 3.6rem;
    font-weight: 800;
    letter-spacing: 0.18em;
    line-height: 1;
  }

  &__jp-heading {
    margin-top: 0.3rem;

    font-size: 1.8rem;
    font-weight: 700;
  }

  &__desc {
    align-self: end;

    font-size: 1.4rem;

    & span {
      display: block;
    }
  }

  &__img {
    display: block;
    height: 100%;
  }
}
</style>
