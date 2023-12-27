<script lang="ts" setup>

import mockData from '~/assets/MockData.json';
import SimpleModal from '~/components/SimpleModal.vue';

const show = ref(false);

function confirm() {
	show.value = false;
}
</script>

<template>
	<section>
		<article @click="show = true" v-for="data in mockData">
			<h3 id="title">{{ data.name }}</h3>
			<hr />
			<p id="mata-data">{{ data.shape }}</p>
			<hr />
			<p v-if="data.description">{{ data.description }}</p>
			<!-- <ModalConfirm v-model="show" title="Hello World!" @confirm="() => confirm()">
				<p>The content of the modal</p>
			</ModalConfirm> -->
			<SimpleModal v-model="show" @confirm="() => confirm()" :name="data.name" :description="data.description" >
				<h1>{{data.name}}</h1>
			</SimpleModal>
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
