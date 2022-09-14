<template lang="pug">
.footer
  ul
    li(v-for="(item, index) in items" :key="index") {{ item }}
  p © 2022 Spotify AB
</template>

<script>
export default {
  name: "FooterComponent",
  data() {
    return {
      items: ["Support", "Privacy", "Terms", "About Spotify premium"],
    };
  },
};
</script>

<style scoped>
.footer {
  @apply w-11/12 lg:w-5/6 mx-auto flex flex-col lg:flex-row justify-between items-center space-y-1.5 lg:space-y-0 mb-11 lg:mb-0;
}

ul {
  @apply flex gap-2.5 text-sm text-gray-600 cursor-pointer;
}

li {
  @apply hover:text-black;
}
</style>
