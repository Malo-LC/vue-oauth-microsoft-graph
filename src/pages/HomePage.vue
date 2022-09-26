<template>
  <h1>Tuto 3 : homePage</h1>
  <div class="flexcolumn">
    <button class="primary" type="button">BaseButton with custom margin</button>
    <button class="disabled" type="button">BaseButton disabled</button>
    <button class="warn" type="button">BaseButton with color props</button>
    <button class="danger" type="button">BaseButton with color props</button>
  </div>
</template>

<script></script>

<style>
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
.flexcolumn {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
