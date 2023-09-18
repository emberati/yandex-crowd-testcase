<script>
export default {
  name: 'circular-text',
  props: {
    size: {
      type: Number,
      required: true
    }
  }
}
</script>
<template>
  <svg
  :width="`${size}px`"
  :height="`${size}px`"
  viewBox="0 0 100 100"
  xmlns="http://www.w3.org/2000/svg"
  >
  <path
    id="circular-text-path"
    d="M90 50C90 72.0914 72.0914 90 50 90C27.9086 90 10 72.0914 10 50C10 27.9086 27.9086 10 50 10C72.0914 10 90 27.9086 90 50Z"
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
  font-size: 13.3px;
  word-spacing: 0.3ch;
  fill: var(--color-main-text);
}
</style>