<template>
	<div class="astro-sell">
		<img src="/astro-sell-2.png" alt="">
		<span class="bubble bubble-bottom-left">
		<slot></slot></span>
	</div>
</template>

<style scoped lang="css">
.astro-sell {
	width: 100%;
	height: 100%;
	display: flex;
	align-items: flex-end;
	justify-content: center;
	position: relative;
}

.astro-sell img {
	height: 80%;
}

.bubble {
	position: absolute;
	bottom: 87%;
	left: 50%;
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