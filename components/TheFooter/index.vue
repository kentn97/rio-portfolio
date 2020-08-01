<template>
  <footer class="footer">
    <div class="footer__wrap">
      <p class="footer__copyright">&copy;copyright 2020, Rio Sugimoto.</p>
      <div class="footer__line"></div>
    </div>
  </footer>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" scoped>
.footer {
  &__wrap {
    display: grid;
    grid-template-columns: repeat(2, max-content);
    align-items: center;
    column-gap: 3rem;
  }

  &__copyright {
    color: rgba($color: $color-black-light, $alpha: 0.3);
    font-weight: 300;
    letter-spacing: 0.1em;
  }

  &__line {
    width: 9rem;
    height: 0.1rem;
    background-color: rgba($color: $color-black-light, $alpha: 0.3);
  }
}
</style>
