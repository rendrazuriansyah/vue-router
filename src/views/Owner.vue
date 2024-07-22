<script setup>
import { useRoute } from "vue-router";
import products from "../data/products.json";

const route = useRoute();
const { owner } = products.find(
	(product) => product.id === parseInt(route.params.id)
);
</script>

<template>
	<div v-if="owner">
		<div>
			<h1>Owner</h1>
			<p>{{ owner.name }}</p>
			<p>{{ owner.email }}</p>
		</div>
	</div>
	<div v-else>Product Not Found</div>
</template>
