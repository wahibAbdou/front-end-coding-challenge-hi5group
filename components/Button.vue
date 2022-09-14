<template lang="pug">
button(type="button" :class="type")
  slot
  span {{ text }}
</template>

<script>
export default {
  name: "ButtonComponent",
  props: {
    text: {
      type: String,
      default: "Default",
    },
    type: {
      type: String,
      default: "primary",
    },
  },
};
</script>

<style scoped>
button {
  @apply flex items-center justify-center gap-1 font-medium rounded-full text-sm px-5 py-2.5 text-center;
}

.primary {
  @apply text-white bg-black hover:bg-black focus:outline-none focus:ring-4 focus:ring-gray-400;
}

.greenish {
  @apply text-black focus:outline-none focus:ring-4 focus:ring-green-400;
  background: #1ccc5c;
}

.greenish:hover {
  background: #18c256;
}
</style>
