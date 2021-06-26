<template>
  <button>{{ text }}</button>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
button {
  min-height: 2rem;
  height: fit-content;
  min-width: 8rem;
  width: fit-content;
  border-radius: 2%;
  font-size: var(--small-font-size);
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  text-align: center;
  cursor: pointer;
  background: white;
  color: black;
  box-shadow: 2px 2px;
  margin-left: 1ch;
  margin-right: 1ch;
}
button:hover{
  animation-name: btn-animation;
  animation-duration: 0.3s;
  animation-fill-mode: forwards;
}
@keyframes btn-animation {
  0% {
    background: white;
    color: black;
  }
  100% {
    background:red;
    color: white;
    transform: scale(0.9, 0.9);
  }
}
</style>
