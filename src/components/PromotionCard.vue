<script>
export default {
  name: 'promotion-card',
  props: {
    iconUrl: {
      type: String,
      required: true
    }
  }
}
</script>

<template>
  <div class="promotion-card">
    <img
      :src="iconUrl"
      alt=""
      class="promotion-icon">
    <p><slot></slot></p>
  </div>
  
</template>

<style>
/* adoptate gap when resolution turning down to 910px */
.promotion-card {
  display: flex;
  /* flex-wrap: wrap; */
  flex-direction: column;

  max-width: 400px;
  gap: 16px;
}

img.promotion-icon {
  max-width: 83px;
  max-height: 83px;

  /* margin-bottom: 16px;
  margin-right: 16px; */
}

@media screen and (max-width: 910px) {
  .promotion-card {
    flex-direction: row;
  }

  .promotion-card > img.promotion-icon,
  .promotion-card > p {
    margin-top: auto;
    margin-bottom: auto;
  }
}
</style>