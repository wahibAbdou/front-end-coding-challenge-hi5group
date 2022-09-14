<template lang="pug">
.checkbox
	input(type='checkbox' :id='forLabel')
	.icon
		iconsCheck
	label(:for='forLabel') {{ label }}
</template>

<script>
export default {
  name: "CheckboxComponent",
  props: {
    label: {
      type: String,
      default: "Default input text",
    },
    forLabel: {
      type: String,
      default: "for-label",
    },
  },
};
</script>

<style scoped>
.checkbox {
  @apply flex items-center;
}

.icon {
  @apply flex flex-shrink-0 justify-center items-center rounded-md w-5 h-5 mr-1 bg-white border-2 border-gray-400  focus-within:border-green-500;
}

label {
  @apply text-sm text-gray-600;
}

input {
  @apply opacity-0 absolute h-5 w-5;
}

input:checked + div {
  border-color: #1ccc5c;
}
input:checked + div svg {
  @apply block;
}
</style>
