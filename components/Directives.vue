<template>

<section class="directives-wrapper" :class="{ 'align-center': $slidev.nav.clicks >= 4 }">

<p v-if="$slidev.nav.clicks <=3" :class="{ 'op-0': !($slidev.nav.clicks === 1) }">There are 5 directives</p>

<p v-if="$slidev.nav.clicks <=3" :class="{ 'op-0': !($slidev.nav.clicks === 2) }">They give you great power</p>

<p v-if="$slidev.nav.clicks <=3" :class="{ 'op-0': !($slidev.nav.clicks === 3) }">Once you master them all</p>

<p v-if="$slidev.nav.clicks === 4" class="center-txt">You can control JS-monster</p>

<img v-if="$slidev.nav.clicks >= 5" src="/directive-pick.png"/>
<div v-if="$slidev.nav.clicks >= 6" class="pick-square" :class="{
	'number-2': $slidev.nav.clicks === 7,
	'number-3': $slidev.nav.clicks === 8,
	'number-4': $slidev.nav.clicks === 9,
}"></div>

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

</style>