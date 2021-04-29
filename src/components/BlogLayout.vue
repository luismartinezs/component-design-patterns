<template>
  <header class="bg-yellow-500 text-white">
    <slot name="header"></slot>
  </header>
  <main class="bg-indigo-500 text-white">
    <slot></slot>
  </main>
  <aside class="bg-green-500 text-white">
    <slot name="sidebar"></slot>
  </aside>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped></style>
