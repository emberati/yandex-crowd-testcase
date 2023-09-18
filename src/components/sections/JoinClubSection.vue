<script>
import YButton from '@/components/YButton';
import PromotionalPrice from '@/components/PromotionalPrice';
import CircularText from '@/components/CircularText';

export default {
  name: 'join-club-section',
  components: {
    YButton,
    PromotionalPrice,
    CircularText
  }
}
</script>

<template>
  <section id="join-club">
    <div class="gradient-background">
      <div class="gradient-white">
        <div class="content">
          <div class="text-wrapper">
            <img
              id="ya-logo"
              :src="require('@/assets/svg/yandex-go-logo.svg')"
              alt=""
              >
            <h1 id="promotion-title">Вступайте в клуб Самокатов</h1>
            <p id="promotion-text">
              Купите абонемент, чтобы стать <br>
              частью клуба в новом сезоне–2024. <br>
              8 месяцев за 
              <promotional-price :newPrice="499" :oldPrice="3190"/>
            </p>
            <y-button>Стать частью клуба</y-button>
          </div>
          <div class="image-wrapper">
            <img
              class="smkt"
              src="@/assets/img/smkt1.png"
              alt="">
            <circular-text
              class="circular-text"
              :size="200">
              сообщество любителей самокатов
            </circular-text>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>

.content {
  display: grid;
  grid-template-columns: max-content auto;
}

.gradient-background {
  background: rgb(255,92,77);
  background: -moz-linear-gradient(90deg, rgba(255,92,77,1) 0%, rgba(235,70,159,1) 25%, rgba(131,65,239,1) 72%, rgba(63,104,249,1) 100%);
  background: -webkit-linear-gradient(90deg, rgba(255,92,77,1) 0%, rgba(235,70,159,1) 25%, rgba(131,65,239,1) 72%, rgba(63,104,249,1) 100%);
  background: linear-gradient(90deg, rgba(255,92,77,1) 0%, rgba(235,70,159,1) 25%, rgba(131,65,239,1) 72%, rgba(63,104,249,1) 100%);
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#ff5c4d",endColorstr="#3f68f9",GradientType=1);
}
.gradient-white {
  background: linear-gradient(180deg, rgba(255, 255, 255, 0.8) 0%, #FFFFFF 100%);
}

section#join-club {
  position: relative;
}

section#join-club .content h1#promotion-title {
  /* max-width: 420px; */
  margin-bottom: 48px;
}

section#join-club .content img#ya-logo {
  margin-bottom: 72px;
}

section#join-club .content p#promotion-text {
  margin-bottom: 44px;
}

.text-wrapper {
  max-width: 390px;
}

.image-wrapper {
  position: relative;
}

.image-wrapper > img.smkt {
  position: absolute;
  z-index: -1;
  margin-left: 50%;
  margin-top: 50%;
  transform: translate(-50%, -50%);

  /* ADDITIONAL ADDJUSTMENT */
  top: -34px;
  left: -15px;
}

.image-wrapper .circular-text {
  position: absolute;
    top: 285px;
    left: 135px;
}

@media screen and (max-width: 916px) {
  .content {
    display: block;
  }

  .text-wrapper {
    max-width: 311px;
  }
  img.smkt {
    width: 353.69px;
    height: 307.6px;
  }

  button {
    display: none;
  }
}
</style>