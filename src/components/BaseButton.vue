<template>
  <button class="flexrow" :class="color" :type="type">
    <slot class="mr" />{{ text }}
  </button>
</template>

<script>
export default {
  name: 'BaseButton',
  props: ['text', 'color', 'type'],
};
</script>

<style scoped>
.danger {
  background-color: #ee373b;
}
.warn {
  background-color: #ff552f;
}

.primary {
  background-color: #29b883;
}
button {
  width: fit-content;
  border: none;
  border-radius: 5px;
  margin: 10px;
  padding: 10px;
  cursor: pointer;
}
.disabled {
  background-color: #29b883;
  opacity: 0.7;
  cursor: not-allowed;
}
.primary:hover {
  background-color: #84ceaf;
}
.primary:focus {
  border: solid black 1px;
}
.flexrow {
  display: flex;
  flex-direction: row;
  align-items: center;
}
.mr {
  margin-right: 10px;
}
</style>
