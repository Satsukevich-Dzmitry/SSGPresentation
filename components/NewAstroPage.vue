<script setup lang="ts">
import Island from './Island.vue'

const props = defineProps()

</script>

<template>
	<div class="divider">
		<Spinner v-if="$slidev.nav.clicks === 0"></Spinner>
		<section class="offer" v-else>
			<Island type="html">
				<template v-slot:icon>
					<img class="logo-img" src="../img/Html.svg" alt="">
				</template>
				<template v-slot:title>HTML</template>
				<div>Im same header. But Astro is MPA. So i am rerendered from scratch
				</div>
			</Island>

			<Island type="react">
				<template v-slot:icon>
					<img class="logo-img" src="../img/React.svg" alt="">
				</template>
				<template v-slot:title>React</template>
				<div>I have to rehydrate again. Too much 💧💧💧!!! And i lost my pretty redux state :(</div>
			</Island>

			<Island type="vue">
				<template v-slot:icon>
					<img class="logo-img" src="../img/Vue.svg" alt="">
				</template>
				<template v-slot:title>Vue</template>
				<div>I wont rehydrate as client only Island. But state is also lost.</div>
			</Island>

			<Island type="svelte">
				<template v-slot:icon>
					<img class="logo-img" src="../img/Svelte.svg" alt="">
				</template>
				<template v-slot:title>Svelte</template>
				<div>And i was smart one. I saved my state to session storage! But now i render on server, hydrate on client
					and re-render after reading data from browser-storage.
				</div>
			</Island>

			<Island type="html">
				<template v-slot:icon>
					<img class="logo-img" src="../img/Html.svg" alt="">
				</template>
				<template v-slot:title>HTML</template>
				<div>I don't have role here. So i just note that inside single page you can use nano-stores to share state
					between frameworks.
				</div>
			</Island>
		</section>
	</div>
</template>

<style scoped lang="css">
.divider {
	width: 100%;
	height: 100%;
}

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