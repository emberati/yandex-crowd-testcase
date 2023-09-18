<script>
export default {
  name: 'event-pictures-grid',
  components: {

  },
  data: () => ({
    images: {
      eventPic1Url: require('@/assets/img/events/event_pic_1.png'),
      eventPic2Url: require('@/assets/img/events/event_pic_2.png'),
      eventPic3Url: require('@/assets/img/events/event_pic_3.png'),
      eventPic4Url: require('@/assets/img/events/event_pic_4.png'),
    },
    icons: {
      bubblesIconUrl: require('@/assets/img/icons/bubbles_icon.png'),
      coffeIconUrl: require('@/assets/img/icons/coffe_icon.png'),
      locatoinIconUrl: require('@/assets/img/icons/location_icon.png')
    }
  })
}
</script>

<template>
<div class="events">
  <div class="image-wrapper">
    <img
      :src="images.eventPic1Url"
      class="event-pic"
      alt=""
    >
    <img
      class="location-icon"
      :src="icons.locatoinIconUrl"
      alt="">
  </div>
  <div class="image-wrapper">
    <img
      :src="images.eventPic2Url"
      class="event-pic"
      alt="">
    <img
      class="bubbles-icon"
      :src="icons.bubblesIconUrl"
      alt="">
  </div>
  <div class="image-wrapper">
    <img
      :src="images.eventPic4Url"
      class="event-pic"
      alt="">
  </div>
  <div class="image-wrapper">
    <img
      :src="images.eventPic3Url"
      class="event-pic"
      alt="">
    <img
      class="coffe-icon"
      :src="icons.coffeIconUrl"
      alt="">
  </div>
</div>
</template>

<style scoped>
.events {
  display: grid;
  grid-template-columns: auto auto;
  gap: 24px;
}

.image-wrapper {
  position: relative;
  /* overflow: hidden; */
  width: 455px;
  height: 455px;
  background-color: var(--color-content-background);
  border-radius: 64px;
}

.image-wrapper:nth-child(2n - 1) {
  animation: shifting1 15s ease-in-out infinite;
}

.image-wrapper:nth-child(2n) {
  animation: shifting2 15s ease-in-out infinite;
}

@keyframes shifting1 {
  0% {
    transform: translateY(0%);
  }

  50% {
    transform: translateY(-5%);
  }

  100% {
    transform: translateY(0%);
  }
}

@keyframes shifting2 {
  0% {
    transform: translateY(-50%);
  }

  50% {
    transform: translateY(-45%);
  }

  100% {
    transform: translateY(-50%);
  }
}

img.event-pic {
  width: 455px;
  height: 455px;
  border-radius: 65px;
}

img[class$=icon] {
  position: absolute;
}

.location-icon {
  left: -60%;
  top: -20%;
  transform: rotate(-15deg);
}

.bubbles-icon {
  right: -33%;
  top: -45%;
  transform: rotate(135.26deg);
}

.coffe-icon {
  right: -50%;
  bottom: -80%;
}

.image-wrapper:nth-child(2n) {
  transform: translateY(-50%);
}
</style>