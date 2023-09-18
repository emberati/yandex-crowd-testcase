<script>
export default {
  name: 'promotional-price',
  props: {
    newPrice: {
      type: Number,
      required: true
    },
    oldPrice: {
        type: Number,
        required: true
    }
  }
}
</script>
<template>
  <span class="promotional-price">
    <div class="wrapper">
      <div class="price new">{{ this.newPrice }}₽</div>
      <div class="price old">{{ this.oldPrice }}₽</div>
    </div>
  </span>
</template>

<style scoped>
.promotional-price {
  display: inline-block;
  
  border-radius: 100px;
  background-color: rgba(255,255,255, 63%);
  background: -moz-radial-gradient(circle at right top, rgba(224,184,255,1) 0%, rgba(182,185,255,1) 100%);
  background: -webkit-radial-gradient(circle at right top, rgba(224,184,255,1) 0%, rgba(182,185,255,1) 100%);
  background: radial-gradient(circle at right top, rgba(224,184,255,1) 0%, rgba(182,185,255,1) 100%);
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#e0b8ff",endColorstr="#b6b9ff",GradientType=1);
}

.price {
  padding: 8px 12px 8px 12px;
  border-radius: 100px;
}

.wrapper {
  display: inline-flex;
  line-height: 16px;
  background-color: rgba(255, 255, 255, 63%);
  border-radius: 100px;
}

.price.new {
  background: rgb(224,184,255);
  background: -moz-radial-gradient(circle at right top, rgba(224,184,255,1) 0%, rgba(182,185,255,1) 100%);
  background: -webkit-radial-gradient(circle at right top, rgba(224,184,255,1) 0%, rgba(182,185,255,1) 100%);
  background: radial-gradient(circle at right top, rgba(224,184,255,1) 0%, rgba(182,185,255,1) 100%);
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#e0b8ff",endColorstr="#b6b9ff",GradientType=1);
}

.price.old {
  font-size: 16px;
  color: #808080;
  text-decoration: line-through;
}
</style>