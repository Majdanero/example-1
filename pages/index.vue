<template lang="pug">
section
	h2 Home
	input(v-model="name")
	p {{nameToAdd}}
	button(@click="AddToList") Add to list
	ul
		li(v-for="(n, ni) in names" :key="ni") {{n}}
</template>
<script setup lang="ts">
	const names = ref([]);
	const name = ref('Kamil');
	const nameToAdd = computed(() => name.value ? `Name: ${name.value}` : '');
	const AddToList = () => {
		names.value.push(nameToAdd.value);
		name.value = '';
	}
</script>
<style lang="scss">
	section {
		h2 {
			color: red;
		}
	}
</style>
