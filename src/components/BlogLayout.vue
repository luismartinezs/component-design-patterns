<template>
  <header>
    <slot name="header"></slot>
  </header>
  <main>
    <slot></slot>
  </main>
  <aside>
    <slot name="sidebar"></slot>
  </aside>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped></style>
