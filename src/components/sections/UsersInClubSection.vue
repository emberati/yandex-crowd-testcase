<script>
import YButton from '@/components/YButton'
import CircularText from '@/components/CircularText';

export default {
  name: 'users-in-club-section',
  components: {
    YButton,
    CircularText
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
      <div class="image-wrapper">
        <circular-text :width="450" :height="450">
          собщество любителей самокатов
        </circular-text>
        <img class="smkt" src="@/assets/img/smkt3.png" alt="">
      </div>
    </div>
  </section>
</template>

<style scoped>
.content {
  display: grid;
  grid-template-columns: max-content auto;
}
.text-wrapper {
  max-width: 390px;
}

.text-wrapper > * {
  margin-bottom: 48px;
} .text-wrapper > *:last-child {margin-bottom: 0;}

.image-wrapper {
  position: relative;
}

img, svg {
  position: absolute;
  
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

svg {
  width: 100%;
  height: 100%;
}
</style>