<script>
import PromotionCard from '@/components/PromotionCard';

export default {
  name: 'promotion-cards-grid',
  components: {
    PromotionCard
  },
  data: () => ({
    images: {
      costStartIconUrl: require('@/assets/svg/icons/0-cost-start-icon.svg'),
      rentsIconUrl: require('@/assets/svg/icons/3x-rents-icon.svg'),
      timerIconUrl: require('@/assets/svg/icons/timer-icon.svg'),
      lowBatteryIconUrl: require('@/assets/svg/icons/low-battery-icon.svg') // buggy svg (invisible battery knippel)
    }
  })
}
</script>

<template>
<div class="promotion">
  <promotion-card :iconUrl="images.costStartIconUrl">
    0 ₽ за старт в каждой поездке
  </promotion-card>
  <promotion-card :iconUrl="images.rentsIconUrl">
    Катаетесь с друзьями? Бронируйте до трёх самокатов с аккаунта с абонементом — так у всех будет бесплатный старт
  </promotion-card>
  <promotion-card :iconUrl="images.timerIconUrl">
      Бесплатная пауза 15 минут в поездке — например, чтобы зайти за кофе или передохнуть
  </promotion-card>
  <promotion-card :iconUrl="images.lowBatteryIconUrl">
      Если самокат недостаточно заряжен или с ним неудобно переходить дорогу, замените по пути на другой — это бесплатно
  </promotion-card>
</div>
</template>

<style>
.promotion {
  display: grid;
  grid-template-columns: repeat(2, minmax(362px, 400px));
  column-gap: 112px;
  row-gap: 61px;
}

.promotion-card:nth-child(2n - 1) {
  max-width: 362px;
}

@media screen and (max-width: 910px) {
  .promotion {
    grid-template-columns: 1fr;
    row-gap: 24px;
    column-gap: normal;
  }
}
</style>