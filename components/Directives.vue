<script setup>
import { computed } from 'vue'

const props = defineProps({
	pageToRun: String
})

const shouldPlay = computed(()=>{
	return props.pageToRun == $slidev.nav.currentPage
})

</script>

<template>

<section class="directives-wrapper" :class="{ 'align-center': $slidev.nav.clicks >= 4 }">

<p v-if="$slidev.nav.clicks <=3" :class="{ 'op-0': !($slidev.nav.clicks === 1) }">There are 5 directives <span class="under-span">川カワキ味阪ミ</span></p>

<p v-if="$slidev.nav.clicks <=3" :class="{ 'op-0': !($slidev.nav.clicks === 2) }">They give you great power <span class="under-span">際閉ぞやン時宣け</span></p>

<p v-if="$slidev.nav.clicks <=3" :class="{ 'op-0': !($slidev.nav.clicks === 3) }">Once you master them all <span class="under-span">載フ週の約店井ゅ</span></p>

<p v-if="$slidev.nav.clicks <= 4" class="center-txt" :class="{ 'op-0': !($slidev.nav.clicks === 4) }">You can control JS-monster <span class="under-span">川カワ阪ミ JS-キ味</span></p>

<img v-if="$slidev.nav.clicks >= 5" src="/directive-pick.png"/>
<div v-if="$slidev.nav.clicks >= 6" class="pick-square" :class="{
	'number-2': $slidev.nav.clicks === 7,
	'number-3': $slidev.nav.clicks === 8,
	'number-4': $slidev.nav.clicks === 9,
}"></div>

<audio autoplay v-if="shouldPlay && $slidev.nav.clicks < 5">
  	<source src="/japanise_sound.mp3" type="audio/mp3">
</audio>

</section>
</template>

<style lang='css' scoped>
.directives-wrapper {
	width: 100%;
	height: 100%;
	display: flex;
	flex-direction: column;
	align-items: flex-start;
	gap: 150px;
	position: relative;
}

.directives-wrapper img {
	width: 92%;
	height: 100%;
}

.pick-square {
	transition: all 1.5s linear;
	position: absolute;
	top: 64px;
	left: 43px;
	border: 5px solid red;
	background: transparent;
	width: 375px;
	height: 192px;
}

.number-2 {
	top: 64px;
	left: 431px;
	width: 382px;
}

.number-3 {
	top: 259px;
	left: 43px;
	width: 376px;
	height: 209px;
}
.number-4 {
	top: 259px;
	left: 431px;
	width: 385px;
	height: 209px;
}

.align-center {
	align-items: center;
	justify-content: center;
}

.directives-wrapper p {
	margin: 0;
	transition: opacity 1s linear;
	font-size: 55px;
	line-height: 60px;
	font-style: italic;
	position: relative
}

.directives-wrapper p:nth-child(2) {
	margin-left: 15px;
}

.directives-wrapper p:nth-child(3) {
	margin-left: 30px;
}
.op-0 {
    opacity: 0;
}

.under-span {
	position: absolute;
	left: 0;
	top: 0;
	color: rgba(255,255,255,0.14);
	z-index: -1;
	font-size: 75px;
	filter: blur(2px);
}

</style>