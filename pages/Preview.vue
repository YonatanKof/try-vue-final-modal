<script setup lang="ts">
import { useModal } from 'vue-final-modal';
import ModalConfirmPlainCss from '~/components/ModalConfirmPlainCss.vue';

const { open, close } = useModal({
	component: ModalConfirmPlainCss,
	attrs: {
		name: 'Hard no!',
		onConfirm() {
			close();
		},
	},
	slots: {
		default: '<p>The content of the modal</p>',
	},
});
</script>

<template>
	<section>
		<h1>Preview</h1>
		<button @click="open">Open Modal</button>
	</section>
</template>
