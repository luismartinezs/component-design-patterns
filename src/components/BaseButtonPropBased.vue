<template>
  <button
    class="flex items-center justify-center bg-blue-500 text-white font-bold text-lg p-4 rounded-md m-1"
    @click="handleClick"
  >
    <div class="flex items-center justify-center">
      <div v-if="showLeftIcon" class="mr-2">
        <LoadingSpinner v-if="isLoading && spinnerSide === 'left'" />
        <AppIcon v-else class="h-8 w-8" />
      </div>

      <span>{{ label }}</span>

      <div v-if="showRightIcon" class="ml-2">
        <LoadingSpinner v-if="isLoading && spinnerSide === 'right'" />
        <AppIcon v-else class="h-8 w-8" />
      </div>
    </div>
  </button>
</template>

<script>
import AppIcon from "@/components/AppIcon.vue";
import LoadingSpinner from "@/components/LoadingSpinner.vue";

export default {
  components: {
    AppIcon,
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
