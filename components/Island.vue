<script setup lang="ts">
const props = defineProps<{
	type: 'react' | 'vue' | 'svelte' | 'html'
}>()
</script>

<template>
	<div class="island" :class="type">
		<div>
			<slot name="icon"></slot>
			<slot name="title"></slot>
		</div>
		<div>
			<slot>Content</slot>
		</div>
	</div>
</template>

<style scoped lang="css">
.island {
	width: 100%;
	max-height: 80px;
	display: flex;
	align-items: center;
	justify-content: flex-start;
	gap: 10px;
	border-radius: 8px;
	padding: 10px;
	transition: all 0.5s linear;
}

.island:hover {
	transform: scale(1.05)
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