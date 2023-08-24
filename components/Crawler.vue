<template>
	<section class="crawler-wrapper">
		<img src="../img/sponge-bob-works.jpeg" class="img-blog" v-if="$slidev.nav.clicks === 4" />
		<img src="../img/sponge-bob-after-hours.jpeg" class="img-blog" v-if="$slidev.nav.clicks === 5" />
		<img src="../img/sponge-bob-result.jpg" class="img-blog" v-if="$slidev.nav.clicks === 6" />
		<img v-if="$slidev.nav.clicks === 12" src="../img/perfect-blog.png" alt="">
		<div class="crawler" v-if="$slidev.nav.clicks >= 7">
			<img src="../img/crawler.png" alt="">
			<span v-if="$slidev.nav.clicks === 7" class="bubble bubble-bottom-left" v-motion-slide-bottom>Sniff-sniff. I'm
				sniffing and try to find best
				websites and show them in Google.
			</span>
			<span v-if="$slidev.nav.clicks === 9" class="bubble bubble-bottom-left">
				What is it?
			</span>
			<span v-if="$slidev.nav.clicks === 11" class="bubble bubble-bottom-left">
				<img src="../img/perfection.jpeg" alt="" />
			</span>
			<span v-if="$slidev.nav.clicks === 12" class="bubble-small bubble-bottom-left">
				It's my job!
			</span>
		</div>
		<div class="page">
			<img v-if="$slidev.nav.clicks === 8" src="../img/web-page.gif" alt="">
			<img v-if="$slidev.nav.clicks === 10" src="../img/lighthouse.jpeg" alt="">
		</div>
	</section>
</template>

<style scoped>
.crawler-wrapper {
	width: 100%;
	display: flex;
	align-items: flex-end;
	justify-content: space-between;
	padding: 0 25px;
	margin-top: 25px;
	min-height: 310px;
}

.crawler {
	width: 150px;
	position: relative;
}

.img-blog {
	height: 325px;
	align-self: center;
	margin: 0 auto;
}

.page img {
	width: 400px;
	height: 300px;
}

.bubble {
	position: absolute;
	bottom: 110%;
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

.bubble-small {
	position: absolute;
	bottom: 110%;
	left: 30%;
	font-family: sans-serif;
	font-size: 18px;
	line-height: 24px;
	width: 100px;
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
	left: 32px;
	bottom: -24px;
}
</style>

<script setup>
</script>