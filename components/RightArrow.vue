<script setup lang="ts">

const props = defineProps<{
	text?: string
}>()

</script>

<template>
	<div class="arrow">
		<div class="arrow-slot">
			<slot><span class="arrow-text">{{ text }}</span></slot>
		</div>
	</div>
</template>
<style lang="css" scoped>
.arrow {
	background: #fff;
	height: 3px;
	width: 350px;
	margin: 0 auto;
	position: relative;
	cursor: pointer;

	&:before,
	&:after {
		content: "";
		background: #fff;
		position: absolute;
		height: 3px;
		width: 15px;
	}

	&:before {
		right: -3px;
		bottom: -4px;
		transform: rotate(-45deg);
	}

	&:after {
		right: -3px;
		top: -4px;
		transform: rotate(45deg);
	}
}

.arrow-text {
	position: absolute;
	left: 50%;
	top: 0;
	transform: translate(-50%, -100%);
	white-space: nowrap;
}

.arrow-slot {
	position: absolute;
	left: 50%;
	top: -5px;
	transform: translate(-50%, -100%);
	white-space: nowrap;
}
</style>