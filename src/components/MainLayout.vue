<script>
import YButton from '@/components/YButton'
import JoinClubSection from '@/components/sections/JoinClubSection';
import PromotionSection from '@/components/sections/PromotionSection';
import ExclusiveEventsSection from '@/components/sections/ExclusiveEventsSection';
import PlusOfferSection from '@/components/sections/PlusOfferSection';
import UsersInClubSection from '@/components/sections/UsersInClubSection';

export default {
  name: 'main-layout',
  components: {
    YButton,
    JoinClubSection,
    PromotionSection,
    ExclusiveEventsSection,
    PlusOfferSection,
    UsersInClubSection
  }
}
</script>

<template>
  <join-club-section />
  <promotion-section />
  <exclusive-events-section />
  <plus-offer-section />
  <users-in-club-section />
  <footer>
    <div class="content">
      <p>
        Доп. опция «Абонемент на самокаты» на 8 месяцев (240 дней) активируется автоматически с момента старта сезона 2024 г.
        самокатов Яндекс Go, далее предусмотрено автопродление доп.опции за 399 руб./мес.
        Сертификат на доп.опцию «Абонемент на самокаты» на 8 месяцев оформляется на условиях документа
        <a href="https://yandex.ru/legal/scooters_seasonpass">yandex.ru/legal/scooters_seasonpass</a>.
        Доп.опция доступна пользователям с активной подпиской (условия подписки:
        <a href="https://yandex.ru/legal/yandex_plus_conditions">yandex.ru/legal/yandex_plus_conditions</a>), 
        есть ограничения, подробнее:
        <a href="https://yandex.ru/legal/yandex_plus_opzii_list">yandex.ru/legal/yandex_plus_opzii_list</a>.
        В случае отсутствия у пользователя активной подписки на дату активации доп.опции, пользователю предоставляется 7 дней подписки
        Яндекс Плюс бесплатно, далее автопродление — 299 руб./мес.
        Электросамокаты Яндекс Go — сервис аренды электросамокатов на условиях:
        <a href="https://clck.ru/gwDGn">clck.ru/gwDGn</a>. 0+
      </p>
    </div>
  </footer>
  <y-button id="floating-join-club-button">Стать частью клуба</y-button>
</template>

<style>
@import '@/assets/css/reset.css';
@import '@/assets/css/fonts.css';
@import '@/assets/css/colors.css';

a, p, span, li, button, input {
  font-family: 'YS Text', sans-serif;
  color: var(--color-main-text);

  font-weight: 500;
  font-size: 24px;
  /* letter-spacing: -0.96px; */
  line-height: 120%;
}

h1, h2, h3 {
  font-family: 'YS Text', sans-serif;
  color: var(--color-main-text);
  margin-bottom: 48px;

  font-weight: 900;
  line-height: 100%;
}

h1 {
  font-size: 72px;
}

h2 {
  font-size: 56px;
}

h3 {
  font-size: 48px;
}

img {
  user-select: none;
  -webkit-user-drag: none;
}

::selection {
  background: var(--color-selection);
}
::-moz-selection {
  background: var(--color-selection);
}

.content {
  position: relative;
  z-index: 1;
  max-width: 916px;
  padding-top: 128px;
  margin-left: auto;
  margin-right: auto;
}

button#floating-join-club-button {
  position: fixed;
  z-index: 2;
  display: none;

  left: 0;
  right: 0;
  bottom: 24px;

  width: 311px;
  margin-left: auto;
  margin-right: auto;

  padding: 18px 0 18px 0;
  font-size: 18px;
  line-height: 16px;
}

footer .content {
  padding-bottom: 128px;
}

footer p,
footer a {
  color: #C5C5C5;
  text-align: justify;
  font-size: 13px;
  font-weight: 400;
  border-bottom: 1px solid transparent;
}

footer a {
  text-decoration: none;
}

footer a:hover {
  color: var(--color-main-accent);
  border-bottom: 1px solid var(--color-main-accent);
  transition: .3s ease;
}

@media screen and (max-width: 916px) {
  .content {
    margin: 0;
    padding: 32px;
    padding-bottom: 0;
  }

  h1 {
    font-size: 36px;
  }

  h2, h3 {
    font-size: 32px;
  }
  
  a, p, span, li, button, input {
    font-size: 16px;
  }

  button#floating-join-club-button {
    display: initial;
  }
}
</style>