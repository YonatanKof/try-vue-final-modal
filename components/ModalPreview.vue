<script setup lang="ts">
import { ModalsContainer, useModal } from 'vue-final-modal';
import SimpleModal from '~/components/SimpleModal.vue';

const props = defineProps<{
    namePreview?: string;
    descriptionPreview?: string;
}>();

const { open, close } = useModal({
	component: SimpleModal,
	attrs: {
		name: props.namePreview,
		description: props.descriptionPreview,
		onConfirm() {
			close();
		},
	},
});
</script>

<template>
	<button @click="open"> Open Modal </button>
	<ModalsContainer />
</template>
