<template>
  <div class="about">
    <div class="about__main-container">
      <BaseHeading1 en-heading="About Me" jp-heading="自己紹介" />
      <img
        src="@/assets/imgs/icon-rio.jpg"
        alt="rio illustration icon"
        class="about__icon"
      />
      <section class="about__rio section-rio">
        <h2 class="section-rio__heading">RIO</h2>
        <p class="section-rio__para">
          <span>愛媛県松山市出身。</span>
          <span
            >高校時代にカリカチュアという技法を使った似顔絵に興味を持ち、絵を描き始める。その後国内最大手の似顔絵の会社に就職し、4年間で約2万人のお客様を作画。講師業・社内技術研修担当・店舗の立ち上げを経験する。</span
          >
        </p>
        <p class="section-rio__para">
          そこで学んだ技術力やコミュニッケーション力をもっと違う分野で活かしたい。もっといろんな分野の絵で幅広く活動していきたい。と思い独立。現在はフリーランスで活動中。
        </p>
      </section>
      <section class="about__portfolio section-portfolio">
        <BaseHeading2>実績</BaseHeading2>
        <HistoryList
          :history-list="PortfolioHistory"
          class="section-portfolio__list"
        />
      </section>
      <section class="about__award section-award">
        <BaseHeading2>コンペティション受賞歴</BaseHeading2>
        <HistoryList
          :history-list="AwardHistory"
          class="section-portfolio__list"
        />
      </section>
    </div>
    <div class="about__sub-container"></div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { PortfolioHistory, AwardHistory } from '~/utils/data'

export default Vue.extend({
  computed: {
    PortfolioHistory() {
      return PortfolioHistory
    },
    AwardHistory() {
      return AwardHistory
    },
  },
})
</script>

<style lang="scss" scoped>
.about {
  display: grid;
  grid-template-columns: 48rem 40rem;
  column-gap: 6rem;

  padding: 6rem 0 6rem 12rem;

  &__main-container {
    position: relative;
  }

  &__icon {
    position: absolute;
    top: -3rem;
    right: 2rem;
    display: block;
    width: 22rem;
    height: 22rem;
  }

  &__rio,
  &__portfolio,
  &__award {
    margin-top: 4rem;
  }

  &__sub-container {
  }
}

.section-rio {
  &__heading {
    margin-bottom: 0.5rem;

    font-family: 'Sansita', sans-serif;
    font-size: 2.8rem;
    font-weight: 800;
    letter-spacing: 0.18em;
  }

  &__para {
    font-weight: 300;
    line-height: 1.5;

    &:not(:first-of-type) {
      margin-top: 3rem;
    }

    & span {
      display: block;
    }
  }
}

.section-portfolio {
  &__list {
    margin-top: 1.5rem;
  }
}
</style>
