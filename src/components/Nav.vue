<script setup>
import { RouterLink } from "vue-router";
</script>

<template>
	<div>
		<!-- Hyperlink: pindah page refresh ulang -->
		<a href="/">Home</a>
		<a href="/about">About</a>
		|
		<!-- Routerlink: pindah page tanpa refresh -->
		<RouterLink to="/">Home</RouterLink>
		<RouterLink to="/about">About</RouterLink>
	</div>
</template>

<style>
div {
	display: flex;
	gap: 20px;
}
</style>
