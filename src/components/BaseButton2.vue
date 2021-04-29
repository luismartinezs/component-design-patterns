<template>
  <button
    class="flex items-center justify-center bg-blue-500 text-white font-bold text-lg p-4 rounded-md m-1"
    @click="handleClick"
  >
    <LoadingSpinner v-if="isLoading" />
    <div v-else class="flex items-center justify-center">
      <!-- Slot based components are less complex than prop based -->
      <slot></slot>
    </div>
  </button>
</template>

<script>
import LoadingSpinner from "@/components/LoadingSpinner.vue";

export default {
  components: {
    LoadingSpinner,
  },
  data() {
    return {
      isLoading: false,
    };
  },
  props: {
    label: {
      type: String,
      default: "Click me",
    },
    showIcon: {
      type: Boolean,
      default: false,
    },
    iconSide: {
      type: String,
      default: "right",
      validator: (value) => ["right", "left", "both"].includes(value),
    },
    spinnerSide: {
      type: String,
      default: "right",
      validator: (value) => ["right", "left"].includes(value),
    },
  },
  methods: {
    handleClick() {
      this.isLoading = true;
      setTimeout(() => {
        this.isLoading = false;
      }, 1000);
    },
  },
  computed: {
    showLeftIcon() {
      return this.showIcon && ["left", "both"].includes(this.iconSide);
    },
    showRightIcon() {
      return this.showIcon && ["right", "both"].includes(this.iconSide);
    },
  },
};
</script>

<style lang="scss" scoped></style>
