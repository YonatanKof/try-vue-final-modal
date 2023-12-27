<template>
	<main>
		<header>
			<h3>Default Layout Header</h3>
		</header>
		<NuxtPage />
		<footer>
			<h3>Default Layout Footer</h3>
		</footer>
	</main>
</template>

<style>
body{
  font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}
main {
  margin: 0 auto;
  display: grid;
  grid-template-rows: auto 1fr auto;
  min-height: 100vh;
  max-width: 800px;
}
</style>