<script>
export default {
  name: 'circular-text',
  props: {
    width: {
      type: Number,
      required: true
    },
    height: {
      type: Number,
      required: true
    }
  }
}
</script>
<template>
  <svg
  :width="`${width}px`"
  :height="`${height}px`"
  viewBox="0 0 100 100"
  xmlns="http://www.w3.org/2000/svg"
  >
  <path
    id="circular-text-path"
    d="M85 50C85 69.33 69.33 85 50 85C30.67 85 15 69.33 15 50C15 30.67 30.67 15 50 15C69.33 15 85 30.67 85 50Z"
    fill="none"/>
    <text class="circular-text">
      <textPath
        
        href="#circular-text-path"
        xlink:href="#circular-text-path">
        <slot></slot>
      </textPath>
    </text>
</svg>
</template>

<style scoped>
text.circular-text {
  transform-origin: center;
  transform: rotate(195deg);
}

textPath {
  font-family: 'YS Text';
  font-weight: 900;
  font-size: 11.7px;
  word-spacing: 0.25ch;
  fill: var(--color-main-text);
}
</style>