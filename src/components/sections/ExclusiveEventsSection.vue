<script>
import EventPicturesGrid from '@/components/EventPicturesGrid'

export default {
  name: 'exclusive-events-section',
  components: {
    EventPicturesGrid
  }
}
</script>

<template>
  <section id="exclusive-events">
    <div class="content">
      <h3>Эксклюзивный доступ к событиям Самокатов</h3>
      <p>
        С абонементом — у вас доступ к специальным мероприятиям, скидки и классный мерч. В 2023 году мы танцевали на Даче Плюс с Антохой MC, катались на самокатах с Сергеем Мезенцевым и слушали хор Attaque de Panique
      </p>
      <event-pictures-grid />
    </div>
  </section>
</template>

<style scoped>
p {
  max-width: 442px;
  margin-bottom: 80px;
}
.events {
  transform: rotate(2deg);
}
</style>