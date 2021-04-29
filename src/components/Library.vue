<template>
  <Book>
    <template #title="slotProps">
      <h1>{{ slotProps.bookTitle }}</h1>
    </template>
  </Book>
</template>

<script>
import Book from "@/components/Book.vue";
export default {
  components: {
    Book,
  },
};
</script>

<style lang="scss" scoped></style>
