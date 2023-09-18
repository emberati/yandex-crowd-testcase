<script>
export default {
  name: 'plus-offer-section',
  components: {

  }
}
</script>

<template>
  <section id="plus-offer">
    <div class="content">
      <div class="text-wrapper">
        <h3>Купить абонемент и вступить в клуб смогут те, кто в Плюсе</h3>
        <p>
          За каждую поездку на самокатах такие пользователи получают кешбэк баллами. Баллы можно тратить на поездки на самокатах и такси с Яндекс Go, покупки и заказы в других сервисах Яндекса
        </p>
      </div>
      <div class="image-wrapper">
        <img class="smkt" src="@/assets/img/smkt2.png" alt="">
        <img class="ya-plus" src="@/assets/img/ya_plus.png" alt="">
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

.image-wrapper {
  position: relative;
}

img.smkt {
  position: absolute;

  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  
  margin: auto;
}

img.ya-plus {
  position: absolute;
  
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;

  margin-top: auto;
  margin-bottom: auto;
  margin-left: 17%;

  transform: rotate(6.06deg);
}
</style>