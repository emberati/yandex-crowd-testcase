<script>
import YButton from '@/components/YButton'
import JoinClubSection from '@/components/sections/JoinClubSection';
import PromotionSection from '@/components/sections/PromotionSection';
import ExclusiveEventsSection from '@/components/sections/ExclusiveEventsSection';
import PlusOfferSection from '@/components/sections/PlusOfferSection';

export default {
  name: 'main-layout',
  components: {
    YButton,
    JoinClubSection,
    PromotionSection,
    ExclusiveEventsSection,
    PlusOfferSection
  }
}
</script>

<template>
  <join-club-section />
  <promotion-section />
  <exclusive-events-section />
  <plus-offer-section />
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