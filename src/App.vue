<template>
  <div class="container mx-auto px-6">
    <!-- Slots and default slots -->
    <div class="flex">
      <BaseButton />
      <BaseButton>
        Cancel
      </BaseButton>
    </div>
    <!-- Named slots -->
    <BlogLayout>
      <template #header>
        <h1>My header</h1>
      </template>
      <p>My main content</p>
      <template #sidebar>
        <h2>My sidebar</h2>
      </template>
    </BlogLayout>
    <AppIcon class="hidden" />
    <!-- Scoped slots providing data to parent -->
    <Library />
  </div>
</template>

<script>
import BaseButton from "@/components/BaseButton.vue";
import BlogLayout from "@/components/BlogLayout.vue";
import AppIcon from "@/components/AppIcon.vue";
import Library from "@/components/Library.vue";

export default {
  name: "App",
  components: { BaseButton, AppIcon, BlogLayout, Library },
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
