<script setup lang="ts">
import { useModal } from 'vue-final-modal';
import SimpleModal from '~/components/SimpleModal.vue';

const { open, close } = useModal({
	component: SimpleModal,
	attrs: {
		name: 'A name',
		description: 'A description',
		onConfirm() {
			close();
		},
	},
});
</script>

<template>
	<section>
		<h1>A single modal</h1>
		<button @click="open">Open Modal</button>
	</section>
</template>
