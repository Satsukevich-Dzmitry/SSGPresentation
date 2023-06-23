<script>
const item1Finish = (el) => {
	el.classList.add('item-1')
}

const item2Finish = (el) => {
	el.classList.add('item-2')
}
const item3Finish = (el) => {
	el.classList.add('item-3')
}
const item4Finish = (el) => {
	el.classList.add('item-4')
}

</script>

<template>
	<div class="wrapper">
		<Transition name="item-1" @after-enter="item1Finish">
			<div class="flip-card item" v-show="$slidev.nav.clicks >= 1">
				<div class="flip-card-inner">
					<div class="flip-card-front">
						Reasons
					</div>
					<ul class="flip-card-back">
						<li>CDN</li>
						<li>CEO</li>
					</ul>
				</div>
			</div>
		</Transition>
		<Transition name="item-2" @after-enter="item2Finish">
			<div class="flip-card item" v-show="$slidev.nav.clicks >= 2">
				<div class="flip-card-inner">
					<div class="flip-card-front">
						Tools
					</div>
					<ul class="flip-card-back">
						<li>Frameworks</li>
						<li>SSG-tools</li>
					</ul>
				</div>
			</div>
		</Transition>
		<Transition name="item-3" @after-enter="item3Finish">
			<div class="flip-card item" v-show="$slidev.nav.clicks >= 3">
				<div class="flip-card-inner">
					<div class="flip-card-front">
						Approaches
					</div>
					<ul class="flip-card-back">
						<li>SSG</li>
						<li>ISR</li>
					</ul>
				</div>
			</div>
		</Transition>
		<Transition name="item-4" @after-enter="item4Finish">
			<div class="flip-card item" v-show="$slidev.nav.clicks >= 4">
				<div class="flip-card-inner">
					<div class="flip-card-front">
						Metrics
					</div>
					<ul class="flip-card-back">
						<li>FCP</li>
						<li>TTI</li>
						<li>TTFB</li>
					</ul>
				</div>
			</div>
		</Transition>
		<div class="item">SSG</div>
	</div>
</template>

<style scoped>
ul li {
	margin: 0;
	list-style: disc;
}

.wrapper {
	margin: 100px auto;
	width: 100%;
	height: 100%;
	position: relative;
}

.item {
	border-radius: 50%;
	background: #fa932d;
	position: absolute;
	top: 20%;
	left: calc(50% - 70px);
	display: flex;
	justify-content: center;
	align-items: center;
	width: 160px;
	height: 160px;
}

.item-1-enter-active {
	transition: transform 0.5s ease;
}

.item-1-enter-to,
.item-1-leave-from,
.item-1-leave-to {
	transform: translate(calc(cos(0) * 220px), calc(sin(0) * -1 * 220px));
}

.item-1-enter-from {
	transform: translate(0, 0);
}

.item-1 {
	transform: translate(calc(cos(0) * 220px), calc(sin(0) * -1 * 220px));
	background: linear-gradient(90deg, rgba(232, 5, 5, 1) 0%, rgba(255, 112, 3, 1) 25%, rgba(247, 221, 10, 1) 49%, rgba(228, 255, 12, 1) 62%, rgba(136, 232, 22, 1) 100%);
}

.item-2-enter-active {
	transition: transform 0.5s ease;
}

.item-2-enter-to,
.item-2-leave-from,
.item-2-leave-to {
	transform: translate(calc(cos(60deg) * 220px), calc(sin(60deg) * -1 * 220px));
}

.item-2-enter-from {
	transform: translate(0, 0);
}

.item-2 {
	transform: translate(calc(cos(60deg) * 220px), calc(sin(60deg) * -1 * 220px));
}

.item-3-enter-active {
	transition: transform 0.5s ease;
}

.item-3-enter-to,
.item-3-leave-from,
.item-3-leave-to {
	transform: translate(calc(cos(120deg) * 220px), calc(sin(120deg * -1) * 220px));
}

.item-3-enter-from {
	transform: translate(0, 0);
}

.item-3 {
	transform: translate(calc(cos(120deg) * 220px), calc(sin(120deg * -1) * 220px));
}

.item-4-enter-active {
	transition: transform 0.5s ease;
}

.item-4-enter-to,
.item-4-leave-from,
.item-4-leave-to {
	transform: translate(calc(cos(180deg) * 220px), calc(sin(180deg * -1) * 220px));
}

.item-4-enter-from {
	transform: translate(0, 0);
}

.item-4 {
	transform: translate(calc(cos(180deg) * 220px), calc(sin(180deg * -1) * 220px));
}

.flip-card {
	background-color: transparent;
	perspective: 1000px;
}

.flip-card-inner {
	position: relative;
	width: 100%;
	height: 100%;
	text-align: center;
	transition: transform 0.8s;
	transform-style: preserve-3d;
	background: transparent;
	border-radius: 50%;
}

.flip-card:hover .flip-card-inner {
	transform: rotateY(180deg);
}

.flip-card-front,
.flip-card-back {
	position: absolute;
	width: 100%;
	height: 100%;
	-webkit-backface-visibility: hidden;
	backface-visibility: hidden;
	border-radius: 50%;
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	gap: 4px;
}

.flip-card-front {
	background: rgb(227, 227, 55);
	color: black;
}

.flip-card-back {
	background: rgb(126, 126, 30);
	color: white;
	transform: rotateY(180deg);
}
</style>