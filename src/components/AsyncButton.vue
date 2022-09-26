<template>
  <base-button
    :disabled="isPending"
    :color="color"
    @click.stop.prevent="handleClick"
    :text="text"
  >
    <p v-if="isPending">rechargement</p>
    <slot />
  </base-button>
</template>

<script>
import BaseButton from './BaseButton.vue';

export default {
  name: 'AsyncButton',
  components: { BaseButton },
  inheritAttrs: false,

  props: {
    color: {
      type: String,
      default: 'primary',
    },
    text: {
      type: String,
    },
    count: {
      type: Number,
    },
  },

  data() {
    return {
      isPending: false,
    };
  },

  methods: {
    handleClick() {
      const originalOnClick = new Promise((resolve) => {
        setTimeout(() => {
          resolve('foo');
        }, 2000);
      });
      this.isPending = true;
      originalOnClick.finally(() => {
        this.isPending = false;
      });
    },
  },
};
</script>
