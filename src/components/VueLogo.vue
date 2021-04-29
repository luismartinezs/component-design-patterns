<template>
  <!-- equivalent to binding :src="..." :alt="..." and @click="..." @mouseover="..." -->
  <img v-bind="imageAttrs" v-on="imageEvents" class="h-24 w-24" />
  <!-- this actually takes more code though, but it can be useful if the bindings of an element are complex and require extra logic -->
  <!-- See NewsFeed component for a use case -->
</template>

<script>
export default {
  data() {
    return {
      imageAttrs: {
        src: "https://vuejs.org/images/logo.png",
        alt: "Vue logo",
      },
    };
  },
  computed: {
    imageEvents() {
      return {
        click: this.handleClick,
        mouseover: this.handleMouseOver,
      };
    },
  },
  methods: {
    handleClick() {
      // do click
    },
    handleMouseOver() {
      // do mouse over
    },
  },
};
</script>

<style lang="scss" scoped></style>
