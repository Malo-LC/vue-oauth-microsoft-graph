<template>
  <h1>Tuto 3 : homePage</h1>
  <div class="flexcolumn">
    <base-button
      color="primary"
      text="BaseButton with custom margin"
      type="button"
    />
    <base-button color="disabled" type="button" text="BaseButton disabled" />
    <base-button
      color="warn"
      type="button"
      text="BaseButton with color props"
    />
    <base-button
      color="danger"
      type="button"
      text="BaseButton with color props"
    />
    <async-button
      :count="handleClickCounter"
      text="AsyncButton with event handler"
      :counter="counter"
    />
  </div>
</template>

<script>
import BaseButton from '../components/BaseButton.vue';
import AsyncButton from '../components/AsyncButton.vue';
export default {
  name: 'homePage',
  components: {
    BaseButton,
    AsyncButton,
  },
  data() {
    return {
      counter: 0,
    };
  },
  methods: {
    handleClickCounter() {
      this.counter += 1;
      console.log(this.counter);
    },
  },
};
</script>

<style>
.flexcolumn {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
