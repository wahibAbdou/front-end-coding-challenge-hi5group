<template lang="pug">
.flex
	.auth
		Header
		Nuxt
		Footer
	SpotifyWeb
</template>

<script>
export default {
  name: "AuthLayout",
};
</script>

<style scoped>
.auth {
  @apply flex-1;
}
</style>
