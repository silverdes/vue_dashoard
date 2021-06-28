<template>
  <div class="relative">
    <button class="flex flex-row space-x-2 focus:outline-none" @click="toggle">
      <slot name="icon"></slot>
      <div class="flex flex-col">
        <slot name="info"></slot>
        <slot name="rank"></slot>
      </div>
    </button>
    <div
      class="
        flex flex-grow
        bg-white
        shadow-md
        rounded-md
        absolute
        top-10
        mt-3
        right-0.5
        border border-gray-100
      "
      v-if="isVisible"
      v-click-away="onClickAway"
    >
      <slot name="dropdown"></slot>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isVisible: false,
    };
  },
  methods: {
    toggle() {
      this.isVisible = !this.isVisible;
    },
    onClickAway() {
      this.isVisible = false;
    },
  },
};
</script>

<style></style>
