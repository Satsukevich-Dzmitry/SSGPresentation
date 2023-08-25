<script setup>
import { computed } from 'vue'

const props = defineProps({
	pageToRun: String
})

const shouldDisplay = computed(()=>{
	return props.pageToRun == $slidev.nav.currentPage
})

</script>

<template>
	<div v-if="$slidev.nav.clicks === 1 && shouldDisplay" class="wrapper-drum">
		<h1 class="font-serif title-by-drum"><slot></slot></h1>
		<audio autoplay>
  			<source src="bass-drop.mp3" type="audio/mp3">
		</audio>
	</div>
</template>
<style lang="css" scoped>
.wrapper-drum {
	width: 100%;
	height: 100%;
	display: flex;
	align-items: center;
	justify-content: center;
}
.title-by-drum {
	color: #f9f9f9;
	font-size: 180px;
	text-shadow: 1px 1px 2px #fffff4;
}
</style>