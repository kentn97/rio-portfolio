<template>
  <div class="header">
    <img src="@/assets/imgs/logo.png" alt="rio-logo" class="header__logo" />
    <nav class="header__nav">
      <ul class="header__list">
        <li class="header__item">
          <n-link to="/" class="header__link">Top</n-link>
        </li>
        <li class="header__item">
          <n-link to="/about" class="header__link">About Me</n-link>
        </li>
        <li class="header__item">
          <n-link to="/works" class="header__link">Works</n-link>
        </li>
        <li class="header__item">
          <n-link to="/order" class="header__btn">Order</n-link>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      activeMenu: '/',
    }
  },
})
</script>

<style lang="scss" scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 2rem;
  padding-bottom: 2rem;

  &__logo {
    height: 4rem;
  }

  &__nav {
    margin-right: 2rem;
  }

  &__list {
    display: grid;
    grid-template-columns: repeat(4, max-content);
    column-gap: 10rem;
    align-items: center;
  }

  &__link,
  &__btn {
    display: block;

    font-family: 'Sansita', sans-serif;
    font-size: 1.8rem;
    letter-spacing: 0.03em;
  }

  &__link {
    transition: color 0.2s;

    &:hover,
    &:focus {
      color: $color-black-light;
    }
  }

  &__link.nuxt-link-exact-active {
    color: $color-green;
  }

  &__btn {
    padding: 1.2rem 4rem;
    color: #fff;
    background-color: $color-skin;

    @include btn-shadow-1;
    transition: filter 0.2s;

    &:hover,
    &:focus {
      filter: brightness(0.95);
    }
  }
}
</style>
