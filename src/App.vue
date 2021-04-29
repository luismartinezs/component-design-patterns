<template>
  <div class="container mx-auto px-6">
    <div class="flex flex-col">
      <BaseButton />
      <BaseButton label="Clicky" />
      <BaseButton label="Clicky" :showIcon="true" />
      <BaseButton label="Clicky" :showIcon="true" iconSide="left" />
      <BaseButton label="Clicky" :showIcon="true" iconSide="both" />
            <BaseButton label="Clicky" :showIcon="true" spinnerSide="right" />
      <BaseButton label="Clicky" :showIcon="true" iconSide="left" spinnerSide="left"  />
    </div>
  </div>
</template>

<script>
import BaseButton from "@/components/BaseButton.vue";
export default {
  name: "App",
  components: { BaseButton },
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
