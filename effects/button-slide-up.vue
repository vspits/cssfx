<template>
<button>Slide</button>
</template>

<style scoped>
button {
  z-index: 1;
  position: relative;
  font-size: inherit;
  font-family: inherit;
  color: white;
  padding: 0.5em 1em;
  outline: none;
  border: none;
  background-color: hsl(246, 41%, 21%);
}

button::before {
  content: '';
  z-index: -1;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: #fc2f70;
  transform-origin: center top;
  transform: scaleY(0);
  transition: transform 0.25s ease-in-out;
}

button:hover {
  cursor: pointer;
}

button:hover::before {
  transform-origin: center bottom;
  transform: scaleY(1);
}
</style>
