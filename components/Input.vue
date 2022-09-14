<template lang="pug">
div
  label(:for='forLabel') {{ label }}
  .relative
    input(:id="forLabel" :type='type' :placeholder='label' v-model="value")
    slot(v-if="value.length > 0")
</template>

<script>
export default {
  name: "InputComponent",
  props: {
    label: {
      type: String,
      default: "Default input text",
    },
    forLabel: {
      type: String,
      default: "for-label-checkbox",
    },
    type: {
      type: String,
      default: "text",
    },
  },
  data() {
    return {
      value: "",
    };
  },
};
</script>

<style scoped>
label {
  @apply block mb-2 text-sm font-medium text-gray-900;
}

input {
  @apply block w-full p-2.5 bg-gray-50 border border-gray-300 text-sm text-gray-900 rounded-lg focus:ring-gray-500 focus:border-gray-500;
}
</style>
