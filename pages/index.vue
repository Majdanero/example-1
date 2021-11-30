<template lang="pug">
section
	h1 Home 1231123123333 1312312312 123123 12312
	p {{message}}
	p {{result}}
	input(v-model="message" )
</template>
<script setup lang="ts">
	const message = ref('Hello');
	const result = computed(() => {
		return message.value + ' computed'
	})
</script>
<style lang="scss">
	section {
		h1 {
			color: red;
		}
	}
</style>