<template>
  <div>
    <component
      v-for="content in apiResponse"
      :key="content.id"
      :is="content.type"
      v-bind="feedItem(content).attrs"
      v-on="feedItem(content).events"
    />
  </div>
</template>

<script>
export default {
  props: ["apiResponse"],
  methods: {
    feedItem(item) {
      if (item.type === "NewsArticle") {
        return {
          attrs: {},
          events: {},
        };
      } else if (item.type === "NewsAd") {
        return {
          attrs: {},
          events: {},
        };
      }
    },
  },
};
</script>

<style lang="scss" scoped></style>
