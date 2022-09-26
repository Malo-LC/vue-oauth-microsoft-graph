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
  },

  data() {
    return {
      isPending: false,
    };
  },

  methods: {
    handleClick() {
      //   const originalOnClick = /** @type {() => Promise<void>} */ (
      //     this.$attrs.onClick
      //   );
      this.isPending = true;
      setTimeout(() => {
        console.log('finished');
        this.isPending = false;
      }, 2000);
    },
  },
};
</script>
