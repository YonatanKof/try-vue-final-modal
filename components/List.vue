<script lang="ts" setup>
import symbolData from '~/assets/FlowchartSymbols.json';
</script>

<template>
	<section>
		<article @click="open" v-for="symbol in symbolData" class="item-hover-less">
			<div class="item-content">
				<h3 id="title">{{ symbol.name }}</h3>
				<hr />
				<p id="mata-data">{{ symbol.shape }}</p>
				<!-- <code>{{ symbol.id }}</code> -->
				<hr />
				<p v-if="symbol.description">{{ symbol.description }}</p>
				<ModalsContainer :title="symbol.name" />
			</div>
			<img loading="lazy" :src="symbol.image" class="this-image" :alt="`The ` + symbol.name + ` symbol`" />
		</article>
	</section>
</template>

<style scoped>
article {
	padding: 1rem;
	background-color: hsl(136, 100%, 95%);
  border-radius: 0.25rem;
}
section {
	display: grid;
	grid-template-columns: 1fr 1fr;
	gap: 1rem;
}
img {
	width: 100%;
	height: auto;
}
</style>
