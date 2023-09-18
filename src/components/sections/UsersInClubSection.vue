<script>
import YButton from '@/components/YButton.vue'

export default {
  name: 'users-in-club-section',
  components: {
    YButton
  }
}
</script>

<template>
  <section id="users-in-club">
    <div class="content">
      <div class="text-wrapper">
        <h3>
          80% наших пользователей уже в клубе и экономят на поездках
        </h3>
        <p>
          Присоединяйтесь — опция начнёт действовать в начале сезона–2024. Об открытии сезона предупредим заранее, чтобы вы были готовы
        </p>
        <y-button>Хочу абонемент</y-button>
      </div>
    </div>
  </section>
</template>

<style scoped>
.text-wrapper {
  max-width: 390px;
}

.text-wrapper > * {
  margin-bottom: 48px;
} .text-wrapper > *:last-child {margin-bottom: 0;}
</style>