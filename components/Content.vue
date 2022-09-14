<template lang="pug">
.content
	h1 Music for everyone!
	p Free music & podcast streaming
	form
		.inputs
			Input(label="Email address or username")
			Input(label="Password" :type="inputType")
				.toggle-input-type(@click="toggleInputType")
					iconsHide(v-if="inputType === 'password'")
					iconsShow(v-else)
			.input-group
				Checkbox(label="Remember for 30 days" )
				a Forgot password?
		.input-group
			Button(text="Login to Spotify" type="greenish")
				iconsLogin
	.text-center
		span.text-gray-700 Don't have an account? 
		a Sign up for free
</template>

<script>
export default {
  name: "ContentComponent",
  data() {
    return {
      inputType: "password",
    };
  },
  methods: {
    toggleInputType() {
      if (this.inputType === "text") {
        this.inputType = "password";
      } else {
        this.inputType = "text";
      }
    },
  },
};
</script>

<style scoped>
.content {
  @apply w-11/12 lg:w-2/5 mx-auto mt-20 mb-14 lg:mt-32 lg:mb-48;
}

h1 {
  @apply font-bold text-4xl text-gray-900;
}

p {
  @apply mb-8 text-gray-700;
}

form {
  @apply mb-4;
}

.inputs {
  @apply space-y-4 mb-8;
}

.input-group {
  @apply flex justify-between items-center;
}

button {
  @apply w-full h-11;
}

a {
  @apply text-black cursor-pointer hover:underline;
}

.toggle-input-type {
  @apply cursor-pointer;
}

.toggle-input-type svg {
  @apply absolute right-2.5;
  top: 50%;
  transform: translateY(-50%);
}
</style>
