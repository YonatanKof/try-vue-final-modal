<script setup lang="ts">
import { ModalsContainer } from 'vue-final-modal';
</script>

<template>
	<main>
		<header>
			<h3>Header</h3>
			<span>
				<nuxt-link to="/">Multiple Modals</nuxt-link> 
				•
				<nuxt-link to="/singlemodal">Single Modal</nuxt-link>
			</span>
		</header>
		<NuxtPage />
		<ModalsContainer />
		<footer>
			<h5>Footer</h5>
		</footer>
	</main>
</template>

<style>
.router-link-active{
	color: green;
	font-weight: bold;
}
header{
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	align-items: center;
}
body {
	font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans',
		'Helvetica Neue', sans-serif;
}
main {
	margin: 0 auto;
	display: grid;
	grid-template-rows: auto 1fr auto;
	min-height: 100vh;
	max-width: 800px;
}
button {
	padding: 0.5em 0.75em;
	text-align: center;
	text-decoration: none;
	border-radius: 0.25em;
}
</style>
