<script>
</script>

<template>
  <button><slot>Button</slot></button>
</template>

<style scoped>
button {
  box-sizing: border-box;
  padding: 24px 48px 24px 48px;

  font-weight: 500;
  border: none;
  border-radius: 36px;
  background-color: var(--color-main-accent);

  box-shadow: 0px 4px 98px 0px var(--color-yellow-semitransparent);

  cursor: pointer;
  outline: none;
  user-select: none;
}

button:hover {
  background: -moz-linear-gradient(45deg, var(--color-main-accent) 0%, var(--color-yellow-bright) 100%);
  background: -webkit-linear-gradient(45deg, var(--color-main-accent) 0%, var(--color-yellow-bright) 100%);
  background: linear-gradient(45deg, var(--color-main-accent) 0%, var(--color-yellow-bright) 100%);
  box-shadow: 0px 4px 98px 0px var(--color-main-accent);
  transition: box-shadow .5s ease;
}
</style>