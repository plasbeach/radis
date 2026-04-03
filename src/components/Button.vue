<script setup>
defineProps({
  label: {
    type: String,
    default: 'Button',
  },
})
</script>

<style scoped>
button {
  font-size: 30px;
  background-color: var(--color-brown-dark);
  color: var(--color-beige);
  text-shadow: 0 2px 0 rgb(0 0 0 / 25%);
  display: inline-flex;
  align-items: center;
  justify-content: center;
  position: relative;
  border: 0;
  z-index: 1;
  user-select: none;
  cursor: pointer;
  text-transform: uppercase;
  letter-spacing: 1px;
  white-space: unset;
  padding: 0.8rem 1.5rem;
  text-decoration: none;
  font-weight: 900;
  transition: all 0.7s cubic-bezier(0, 0.8, 0.26, 0.99);
}

button:before {
  position: absolute;
  pointer-events: none;
  top: 0;
  left: 0;
  display: block;
  width: 100%;
  height: 100%;
  content: '';
  transition: 0.7s cubic-bezier(0, 0.8, 0.26, 0.99);
  z-index: -1;
  background-color: var(--color-brown-dark) !important;
  box-shadow:
    0 -4px var(--color-brown-deep) inset,
    0 4px var(--color-brown-mid) inset,
    -4px 0 var(--color-brown-mid) inset,
    4px 0 var(--color-brown-deep) inset;
}

button:after {
  position: absolute;
  pointer-events: none;
  top: 0;
  left: 0;
  display: block;
  width: 100%;
  height: 100%;
  content: '';
  box-shadow: 0 4px 0 0 rgb(0 0 0 / 15%);
  transition: 0.7s cubic-bezier(0, 0.8, 0.26, 0.99);
}

button:hover:before {
  box-shadow:
    0 -4px rgb(0 0 0 / 70%) inset,
    0 4px rgb(255 255 255 / 30%) inset,
    -4px 0 rgb(255 255 255 / 30%) inset,
    4px 0 rgb(0 0 0 / 70%) inset;
}

button:hover:after {
  box-shadow: 0 4px 0 0 rgb(0 0 0 / 15%);
}

button:active {
  transform: translateY(10px);
}

button:active:after {
  box-shadow: 0 0px 0 0 rgb(0 0 0 / 15%);
}
</style>

<template>
  <button>{{ label }}</button>
</template>
