<template>
  <h1>Tuto 3 : homePage</h1>
  <button class="defaultButton" type="button">
    BaseButton with custom margin
  </button>
  <button class="disabledButton" type="button">BaseButton disabled</button>
</template>

<script></script>

<style>
.defaultButton {
  background-color: #29b883;
  border: none;
  border-radius: 5px;
  margin: 10px;
  padding: 10px;
  cursor: pointer;
}
.disabledButton {
  background-color: #29b883;
  opacity: 0.7;
  border: none;
  border-radius: 5px;
  margin: 10px;
  padding: 10px;
  cursor: not-allowed;
}
.defaultButton:hover {
  background-color: #84ceaf;
}
.defaultButton:focus {
  border: solid black 1px;
}
</style>
