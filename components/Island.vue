<script setup lang="ts">
const props = defineProps<{
	type: 'react' | 'vue' | 'svelte' | 'html'
}>()
</script>

<template>
	<div class="island" :class="type">
			<slot name="icon"></slot>
			<slot name="title"></slot>
	</div>
</template>

<style scoped lang="css">
.island {
	width: 100%;
	height: 100%;
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	gap: 6px;
	border-radius: 8px;
	padding: 10px;
}

.vue {
	border: green 1px solid;
}

.react {
	border: blue 1px solid;
}

.svelte {
	border: orange 1px solid;
}

.html {
	border: white 1px solid;
}
</style>