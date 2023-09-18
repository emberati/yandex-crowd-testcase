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
      <div class="image-wrapper">
        <div class="text-around-image">
          <img class="smkt" src="@/assets/img/smkt3.png" alt="">
          <circular-text :size="450">
            собщество любителей самокатов
          </circular-text>
        </div>
      </div>
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
.content {
  display: grid;
  grid-template-columns: auto max-content;
}
.text-wrapper {
  max-width: 390px;
}

.text-wrapper > * {
  margin-bottom: 48px;
} .text-wrapper > *:last-child {margin-bottom: 0;}
/* 
.image-wrapper {
  position: relative;
} */

.text-around-image {
  position: relative;
  width: 450px;
  height: 450px;
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

@media screen and (max-width: 916px) {
  .content {
    display: block;
  }

  .text-around-image {
    width: 311px;
    height: 311px;
  }
}
</style>