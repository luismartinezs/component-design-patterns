<template>
  <div class="book">
    <slot name="title" :bookTitle="bookTitle"></slot>
    <slot name="description" :bookDescription="bookDescription"></slot>
  </div>
</template>

<script>
export default {
  data() {
    return {
      bookTitle: "Child providing data",
      bookDescription: "Lorem ipsum dolor sit amet this is a description"
    };
  },
};
</script>

<style lang="scss" scoped></style>
