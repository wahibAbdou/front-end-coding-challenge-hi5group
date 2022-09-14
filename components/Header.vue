<template lang="pug">
.header
	Logo
	Button(text="Download the Desktop App")
		iconsDownload
</template>

<script>
export default {
  name: "HeaderComponent",
};
</script>

<style scoped>
.header {
  @apply w-11/12 lg:w-5/6 mx-auto mt-11 lg:mt-24 flex items-center justify-between;
}

button {
  @apply hidden lg:flex;
}
</style>
