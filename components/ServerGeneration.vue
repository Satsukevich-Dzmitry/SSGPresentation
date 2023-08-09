<script setup lang="ts">
</script>

<template>
	<section class="wrapper">
		<div v-if="$slidev.nav.clicks >= 2" class="code"><img src="../img/code.jpg" alt=""></div>
		<div v-if="$slidev.nav.clicks >= 3" class="plus">+</div>
		<div v-if="$slidev.nav.clicks >= 4" class="server"><img src="../img/server-svg.svg" alt=""></div>
		<div v-if="$slidev.nav.clicks >= 5" class="equal">=</div>
		<div v-if="$slidev.nav.clicks >= 6" class="html"><img src="../img/html-code.jpeg" alt=""></div>
	</section>
</template>

<style scoped lang="css">
.wrapper {
	width: 100%;
	height: 100%;
	position: relative;
	display: flex;
	align-items: center;
	padding: 0 0 120px 0;
	justify-content: flex-start;
	gap: 15px;
}

.code img {
	width: 300px;
}

.server img {
	width: 185px;
}

.html img {
	width: 300px;
}
</style>