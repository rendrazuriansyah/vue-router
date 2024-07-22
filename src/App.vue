<script setup>
import { ref } from "vue";
import { RouterView } from "vue-router";
import Nav from "./components/Nav.vue";

const count = ref(0);
</script>

<template>
	<Nav />
	<button @click="count++">Count: {{ count }}</button>
	<main>
		<RouterView />
	</main>
</template>
