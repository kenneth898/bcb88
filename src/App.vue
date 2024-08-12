<!-- src/App.vue -->
<template>
	<div style="position: relative;" id="app">
		<header style="position: sticky; top: 0; z-index: 2;">
			<top />
		</header>
		<main>
			<router-view></router-view>
		</main>
		<footer>
			<bottom />
		</footer>
	</div>
</template>

<script>
import bottom from './components/Bottomm.vue';
import top from './components/Topp.vue';
export default {
	name: 'App',
	components: {
		bottom,
		top
	}
};
</script>
<style scoped></style>