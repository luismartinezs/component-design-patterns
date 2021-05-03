<template>
  <Book>
    <!-- If there is only one slot, we could put the v-slot (#) attr in the <Book #title>, but it's easier to just stick to <template #title> -->
    <!-- slotProps is only scoped to the slot -->
    <template #title="{ bookTitle }">
      <h1>{{ bookTitle }}</h1>
    </template>
    <template #description="{bookDescription}">
      <p>{{ bookDescription }}</p>
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
