<template>
  <div class="container mx-auto px-6">
    <AppIcon class="hidden" />
    <div class="flex">
      <BaseButton />
      <BaseButton>
        Cancel
      </BaseButton>
    </div>
  </div>
</template>

<script>
import BaseButton from "@/components/BaseButton.vue";
import AppIcon from "@/components/AppIcon.vue";

export default {
  name: "App",
  components: { BaseButton, AppIcon },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
