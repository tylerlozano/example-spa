<template>
  <button
    :style="{ background: background, color: color }"
    @click="$emit('my-event')"
  >
    My Button
  </button>
</template>

<script>
export default {
  props: {
    color: {
      type: String,
      required: true,
    },
    background: {
      type: String,
      required: false,
    },
  },
};
</script>