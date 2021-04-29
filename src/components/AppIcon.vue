<template>
  <div>
    <ArrowCircleRightIcon />
  </div>
</template>

<script>
import { ArrowCircleRightIcon } from "@heroicons/vue/solid";

export default {
  props: {
    iconName: {
      type: String,
      required: true,
    },
  },
  components: { ArrowCircleRightIcon },
};
</script>
