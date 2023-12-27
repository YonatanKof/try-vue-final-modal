<script lang="ts" setup>
import mockData from '~/assets/MockData.json';
</script>

<template>
	<section>
		<article v-for="data in mockData">
			<h3 id="title">{{ data.name }}</h3>
			<hr />
			<p id="mata-data">{{ data.shape }}</p>
			<hr />
			<p v-if="data.description">{{ data.description }}</p>
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
</style>
