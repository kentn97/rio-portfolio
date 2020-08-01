<template>
  <a :href="snsData.link" target="_blank" class="sns-block" :class="sns">
    <img
      :src="require(`@/assets/imgs/${snsData.imgName}`)"
      :alt="sns + ' icon'"
      class="sns-block__logo"
    />
    <p class="sns-block__id">{{ snsData.id }}</p>
  </a>
</template>

<script lang="ts">
import Vue from 'vue'

interface SnsInfo {
  id: string
  imgName: string
  link: string
}

const getSnsInfo: (sns: string) => SnsInfo = sns => {
  switch (sns) {
    case 'twitter':
      return {
        id: 'Riomaruart',
        imgName: 'icon-twitter.svg',
        link: 'https://twitter.com/Riomaruart',
      }
    case 'instagram':
      return {
        id: 'rio_oneart',
        imgName: 'icon-instagram.svg',
        link: 'https://www.instagram.com/rio_oneart/',
      }
    case 'email':
      return {
        id: 'rio_oneart@gmail.com',
        imgName: 'icon-email.svg',
        link: 'mailto:rio_oneart@gmail.com',
      }
    default:
      return {
        id: 'Riomaruart',
        imgName: 'icon-twitter.svg',
        link: 'https://twitter.com/Riomaruart',
      }
  }
}

export default Vue.extend({
  props: {
    sns: {
      type: String,
      required: true,
    },
  },
  computed: {
    snsData() {
      return getSnsInfo(this.sns)
    },
  },
})
</script>

<style lang="scss" scoped>
.sns-block {
  display: grid;
  grid-template-columns: repeat(2, max-content);
  align-items: center;
  justify-content: start;
  column-gap: 0.8rem;

  padding: 1rem;

  transition: background 0.2s;

  &__logo {
    padding: 0.5rem;

    border-radius: 50%;
  }

  &__id {
    font-size: 1.5rem;
    font-weight: 500;
  }

  &.twitter {
    background-color: rgba($color: #1da1f2, $alpha: 0.1);

    &:hover,
    &:focus {
      background-color: rgba($color: #1da1f2, $alpha: 0.2);
    }

    & .sns-block__logo {
      background-color: #1da1f2;
    }

    & .sns-block__id {
      color: #1da1f2;
    }
  }

  &.instagram {
    background-color: rgba($color: #f77737, $alpha: 0.1);

    &:hover,
    &:focus {
      background-color: rgba($color: #f77737, $alpha: 0.2);
    }

    & .sns-block__logo {
      background-color: #f77737;
    }

    & .sns-block__id {
      color: #f77737;
    }
  }

  &.email {
    background-color: rgba($color: #999999, $alpha: 0.1);

    &:hover,
    &:focus {
      background-color: rgba($color: #999999, $alpha: 0.2);
    }

    & .sns-block__logo {
      background-color: #999999;
    }

    & .sns-block__id {
      color: #999999;
    }
  }
}
</style>
