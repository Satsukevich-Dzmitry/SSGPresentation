<script setup>
import RightArrow from './RightArrow.vue';
import StaticPage from './StaticPage.vue'

</script>

<template>
	<div class="wrapper">
		<div>
			<div class="toogled-image">
				<img src="../img/React.svg" alt="" class="image" :class="{
					'image_hidden': $slidev.nav.clicks >= 4
				}">
				<img src="../img/Next.svg" alt="" class="image" :class="{
					'image_hidden': $slidev.nav.clicks < 4
				}">
				<RightArrow v-if="$slidev.nav.clicks >= 5" v-motion-slide-left class="arrow">
					Just code and everything else
					handled for you</RightArrow>
			</div>
			<div class="toogled-image">
				<img src="../img/Vue.svg" alt="" class="image" :class="{
					'image_hidden': $slidev.nav.clicks >= 4
				}">
				<img src="../img/Nuxt.svg" alt="" class="image" :class="{
					'image_hidden': $slidev.nav.clicks < 4
				}">
				<RightArrow v-if="$slidev.nav.clicks >= 6" v-motion-slide-left class="arrow">Type one command</RightArrow>
			</div>
			<div class="toogled-image">
				<img src="../img/Svelte.svg" alt="" class="image">
				<p class="kit" :class="{
					'kit_visible': $slidev.nav.clicks >= 4
				}">Kit</p>
				<RightArrow v-if="$slidev.nav.clicks >= 7" v-motion-slide-left class="arrow">Add adapter</RightArrow>
			</div>
			<div class="toogled-image">
				<img src="../img/Angular.svg" alt="" class="image">
				<span class="emoji face" :class="{
					'emoji_visible': $slidev.nav.clicks >= 4
				}">😎</span>
				<p class="emoji finger" :class="{
					'emoji_visible': $slidev.nav.clicks >= 4
				}">👍</p>
				<RightArrow v-if="$slidev.nav.clicks >= 8" v-motion-slide-left class="arrow">???</RightArrow>
			</div>
		</div>
		<StaticPage v-if="$slidev.nav.clicks >= 9 && $slidev.nav.clicks < 17" v-motion-slide-left></StaticPage>
		<div class="astro" v-if="$slidev.nav.clicks >= 17"><img class="astro-img" src="../img/astro.svg" alt=""> <span
				v-if="$slidev.nav.clicks === 17" class="bubble bubble-bottom-left">
				Don't forget about me 😏</span></div>
		<p class="astro_joined" v-if="$slidev.nav.clicks == 16">ASTRO joined chat</p>
	</div>
</template>

<style scoped lang="css">
.image {
	width: 75px;
	height: 75px;
	position: absolute;
	transition: opacity 1.5s linear;
}

.image_hidden {
	opacity: 0;
}

.kit {
	color: #ff3e00;
	font-weight: 900;
	font-size: 2rem;
	position: absolute;
	left: 0;
	top: 10px;
	opacity: 0;
	transition: all 1.5s linear;
}

.kit_visible {
	left: 90%;
	opacity: 1;
}

.emoji {
	font-size: 2rem;
	transition: all 0.5s linear;
	position: absolute;
	opacity: 0;
}

.emoji_visible {
	opacity: 1;
}

.face {
	top: 20%;
	left: 28%;
}

.astro_joined {
	position: absolute;
	color: blue;
	background: gray;
	padding: 6px;
	border-radius: 12px;
	top: 110%;
	left: 80%;
}

.finger {
	top: 10%;
	left: 80%;
}

.toogled-image {
	width: 75px;
	height: 75px;
	position: relative;
}

.arrow {
	position: absolute;
	width: 450px;
	top: 50%;
	left: 120px;
}

.wrapper {
	display: flex;
	justify-content: space-between;
	position: relative;
}

.astro {
	position: relative;
}

.astro-img {
	width: 240px;
}

.bubble {
	position: absolute;
	bottom: 110%;
	left: 20%;
	font-family: sans-serif;
	font-size: 18px;
	line-height: 24px;
	width: 250px;
	background: #fff;
	border-radius: 40px;
	padding: 20px;
	text-align: center;
	color: #000;
}

.bubble-bottom-left:before {
	content: "";
	width: 0px;
	height: 0px;
	position: absolute;
	border-left: 24px solid #fff;
	border-right: 12px solid transparent;
	border-top: 12px solid #fff;
	border-bottom: 20px solid transparent;
	left: 75px;
	bottom: -30px;
}
</style>