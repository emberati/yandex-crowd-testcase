<script>
import PromotionCardsGrid from '@/components/PromotionCardsGrid';

export default {
  name: 'promotion-section',
  components: {
    PromotionCardsGrid
  }
}
</script>
<template>
  <section id="promotion">
    <div class="content">
      <h2>Вот что даёт участие в клубе</h2>
      <promotion-cards-grid />
    </div>
  </section>
</template>
<style scoped>
section#join-club .content img#ya-logo {
  width: 112.35px;
  height: 32px;
  margin-bottom: 32px;
}

section#join-club .content h1#promotion-title {
  margin-bottom: 35px;
}

section#join-club .content p#promotion-text {
  font-size: 18px;
}
</style>