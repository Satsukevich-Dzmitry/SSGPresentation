<script setup lang="ts">
import RightArrow from './RightArrow.vue';
import Spinner from './Spinner.vue';
import LeftArrow from './LeftArrow.vue';

</script>

<template>
	<section class="wrapper">
		<div class="me">
			<img src="../img/me.png" alt="">
			<span v-if="$slidev.nav.clicks === 1" class="bubble bubble-bottom-left" v-motion-slide-bottom>Hmmm, wonder if
				there are any new cool
				posts on my favorite
				sponge-blog.com</span>
			<span v-if="$slidev.nav.clicks === 6" class="bubble bubble-bottom-left" v-motion-slide-bottom>Wow. It was so
				<span class="blazingly-fast">Blazingly fast</span></span>
			<span v-if="$slidev.nav.clicks === 7" class="bubble bubble-bottom-left" v-motion-slide-bottom>I want to write a comment. So it's time to login.</span>
			<span v-if="$slidev.nav.clicks === 10" class="bubble bubble-bottom-left" v-motion-slide-bottom>Fast as always!
				Take my mon... creds</span>
		</div>
		<RightArrow v-motion-slide-left v-if="$slidev.nav.clicks === 2">
			<div class="typewriter">
				<p>sponge-blog.com</p>
			</div>
		</RightArrow>
		<LeftArrow text="Here is index.html" v-motion-slide-right
			v-if="$slidev.nav.clicks >= 5 && $slidev.nav.clicks <= 6" />
		<RightArrow text="Give me login page" v-motion-slide-left v-if="$slidev.nav.clicks === 8">
			<div class="typewriter-2">
				<p>sponge-blog.com/login</p>
			</div>
		</RightArrow>
		<LeftArrow text="Here is login.html" v-motion-slide-right
			v-if="$slidev.nav.clicks >= 9 && $slidev.nav.clicks <= 10" />
		<RightArrow text="Credentials" v-motion-slide-left v-if="$slidev.nav.clicks === 11" />
		<div class="him">
			<Spinner v-if="$slidev.nav.clicks === 3"></Spinner>
			<img src="../img/cdn.png" alt="" class="me" v-if="$slidev.nav.clicks >= 4" v-motion-pop>
			<span v-if="$slidev.nav.clicks === 12" class="right-bubble bubble-bottom-right" v-motion-slide-bottom>
				My job is done. After you login everything will be personalised. And user-specific pages will be CSR or SSR.
			</span>
			<span v-if="$slidev.nav.clicks === 13" class="right-bubble bubble-bottom-right" v-motion-slide-bottom>
				<img src="../img/frog.webp" class="frog" />
				Visit next meetup to learn SSR
			</span>
		</div>
	</section>
</template>

<style scoped lang="css">
.wrapper {
	width: 100%;
	height: 100%;
	position: relative;
	display: flex;
	align-items: center;
	justify-content: space-between;
}

.me {
	aspect-ratio: auto;
	width: 200px;
	justify-self: flex-start;
	position: relative;
}

.him {
	aspect-ratio: auto;
	position: relative;
	width: 200px;
}

.bubble {
	position: absolute;
	bottom: 120%;
	left: 30%;
	font-family: sans-serif;
	font-size: 18px;
	line-height: 24px;
	width: 300px;
	background: #fff;
	border-radius: 40px;
	padding: 20px;
	text-align: center;
	color: #000;
}

.right-bubble {
	position: absolute;
	bottom: 120%;
	left: -30%;
	font-family: sans-serif;
	font-size: 18px;
	line-height: 24px;
	width: 300px;
	background: #fff;
	border-radius: 40px;
	padding: 20px;
	text-align: center;
	color: #000;
}

.bubble-bottom-right:before {
	content: "";
	width: 0px;
	height: 0px;
	position: absolute;
	border-left: 24px solid #fff;
	border-right: 12px solid transparent;
	border-top: 12px solid #fff;
	border-bottom: 20px solid transparent;
	right: 32px;
	bottom: -24px;
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
	left: 32px;
	bottom: -24px;
}

.blazingly-fast {
	background: linear-gradient(90deg, rgba(86, 149, 255, 1) 0%, rgba(65, 65, 203, 1) 23%, rgba(176, 51, 51, 1) 100%);
	background-clip: text;
	-webkit-background-clip: text;
	color: transparent;
}

.typewriter {
	width: 210px;
	border-radius: 30px;
	border: 1px solid #dcdcdc;
	display: flex;
	flex-direction: row;
	padding: 0 15px;
	align-items: center;
	justify-content: flex-start;
}

.typewriter p {
	overflow: hidden;
	width: 210px;
	border-right: .15em solid white;
	white-space: nowrap;
	margin: 0 auto;
	letter-spacing: .15em;
	animation:
		typing 1.5s steps(40, end),
		blink-caret .75s step-end infinite;
}

.typewriter-2 {
	width: 270px;
	border-radius: 30px;
	border: 1px solid #dcdcdc;
	display: flex;
	flex-direction: row;
	padding: 0 15px;
	align-items: center;
	justify-content: flex-start;
}

.typewriter-2 p {
	overflow: hidden;
	width: 270px;
	border-right: .15em solid white;
	white-space: nowrap;
	margin: 0 auto;
	letter-spacing: .15em;
	animation:
		typing 1.5s steps(40, end),
		blink-caret .75s step-end infinite;
}

/* The typing effect */
@keyframes typing {
	from {
		width: 0
	}

	to {
		width: 100%
	}
}

/* The typewriter cursor effect */
@keyframes blink-caret {

	from,
	to {
		border-color: transparent
	}

	50% {
		border-color: orange;
	}
}

.frog {
	height: 110px;
	margin: 0 auto;
}
</style>