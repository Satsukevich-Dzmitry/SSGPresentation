<script setup lang="ts">
import { ref } from 'vue'

const rawHtml = `
<html>
<head>
...	
</head>

<body>
	<div>
		Static content
	</div>
</body>
</html>

`

const counter = ref(0)

const increment = () => counter.value = counter.value + 1

</script>

<template>
	<div class="wrapper-html">
		<img v-if="$slidev.nav.clicks == 10" class="objection" v-motion-pop src="../img/objection.png" />
		<img v-if="$slidev.nav.clicks >= 11" class="objection" src="../img/not-only-static.png" />
		<span v-if="$slidev.nav.clicks === 11" class="bubble bubble-bottom-left">After we generate
			page it is not static!</span>
		<span v-if="$slidev.nav.clicks === 12" class="bubble bubble-bottom-left">
			This will also work! <br />
			Count: {{ counter }}
			<br /> <button class="increment" type="button" @click="increment">+</button></span>
		<span v-if="$slidev.nav.clicks === 13" class="bubble bubble-bottom-left">
			Why?</span>
		<span v-if="$slidev.nav.clicks === 14" class="bubble bubble-bottom-left">
			Because after we generate page we don't throw away JS. So all this interactions will still work.</span>
		<span v-if="$slidev.nav.clicks === 15" class="bubble bubble-bottom-left">
			More then that, after <span>HYDRATION</span> we will get SPA. Only first page is SSGed</span>
		<pre v-if="$slidev.nav.clicks == 9">{{ rawHtml }}</pre>
	</div>
</template>

<style scoped lang="css">
.wrapper-html {
	background-color: white;
	color: black;
	padding: 0 5px 0 15px;
	border-radius: 8px;
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
}

.objection {
	max-width: 250px;
	max-height: 131px;
}

.bubble {
	position: absolute;
	bottom: 80%;
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
	border: 1px solid black;
}

.bubble-bottom-left:before {
	content: "";
	width: 0px;
	height: 0px;
	position: absolute;
	border-left: 24px solid #000;
	border-right: 12px solid transparent;
	border-top: 12px solid #000;
	border-bottom: 20px solid transparent;
	left: 75px;
	bottom: -32px;
}

.increment {
	border: 1px solid #000;
	border-radius: 8px;
	width: 36px;
	height: 36px;
	text-align: center;
}
</style>