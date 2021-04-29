<template>
  <div class="container mx-auto px-6">
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
import BlogLayout from "@/components/BlogLayout.vue";
import AppIcon from "@/components/AppIcon.vue";

export default {
  name: "App",
  components: { BaseButton, AppIcon, BlogLayout },
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
