<script setup lang="ts">
import Island from './Island.vue'

const props = defineProps()

</script>

<template>
	<section class="offer">
		<v-click>
			<Island type="html">
				<template v-slot:icon>
					<img class="logo-img" src="../img/Html.svg" alt="">
				</template>
				<template v-slot:title>HTML</template>
				<div>Im just static header. And i dont need JS to provide <a href="#">Link with {{ '<a>' }} tag</a></div>
			</Island>
		</v-click>
		<v-click>
			<Island type="react">
				<template v-slot:icon>
					<img class="logo-img" src="../img/React.svg" alt="">
				</template>
				<template v-slot:title>React</template>
				<div>I used to show interactive ads, so i loaded with <span class="directive">client:load</span>. Already
					send
					all about you to google!</div>
			</Island>
		</v-click><v-click>
			<Island type="vue">
				<template v-slot:icon>
					<img class="logo-img" src="../img/Vue.svg" alt="">
				</template>
				<template v-slot:title>Vue</template>
				<div>I render online chat with websockets. No need to generate me on server, so im <span
						class="directive">client:only=<span class="vue-text">"vue"</span></span>.</div>
			</Island>
		</v-click>
		<v-click>
			<Island type="svelte">
				<template v-slot:icon>
					<img class="logo-img" src="../img/Svelte.svg" alt="">
				</template>
				<template v-slot:title>Svelte</template>
				<div>I render feedback form. But noone use me, so i can wait with <span class="directive">client:idle</span>
					or
					<span class="directive">client:visible</span>
				</div>
			</Island>
		</v-click>
		<v-click>
			<Island type="html">
				<template v-slot:icon>
					<img class="logo-img" src="../img/Html.svg" alt="">
				</template>
				<template v-slot:title>HTML</template>
				<div>Im just static footer. And i also just render some links
					<Link to="9">Link to next slide :)</Link>
				</div>
			</Island>
		</v-click>
	</section>
</template>

<style scoped lang="css">
.offer {
	width: 100%;
	height: 100%;
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: flex-start;
	gap: 10px;
}

.logo-img {
	height: 40px;
	width: 40px;
}

.directive {
	color: rgba(255, 167, 2, 0.712);
	text-decoration: underline;
}


.vue-text {
	color: green;
}
</style>