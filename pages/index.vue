<!--suppress ALL -->
<template lang="pug">
section
	h2 Home
	input(v-model="width" type="range" min="0" max="100")
	br
	input(v-model="name")
	p {{nameToAdd}}
	button(@click="AddToList") Add to list
	ul
		li(v-for="(n, ni) in names" :key="ni") {{n}}
</template>
<script setup lang="ts">
	const width = ref(50);
	const width_style = computed(() => Math.max(50, width.value * 3) + 'px');
	const names = ref([]);
	const name = ref('Kamil');
	const color = ref('orangered');
	const nameToAdd = computed(() => name.value ? `Name: ${name.value}` : '');
	const AddToList = () => {
		names.value.push(nameToAdd.value);
		name.value = '';
	}
</script>
<style scoped lang="scss">
	section {
		p {
			display: flex;
			background-color: red;
			width: v-bind('width_style');
		}
		h2 {
			color: red;
			color: v-bind('color');
		}
	}
</style>
