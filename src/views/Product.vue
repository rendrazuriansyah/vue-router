<script setup>
import { useRoute, RouterView } from "vue-router";
import products from "../data/products.json";

const route = useRoute();
const product = products.find(
	(product) => product.id === parseInt(route.params.id)
);
</script>

<template>
	<div>
		<h1>Product</h1>
		<div>
			<h2>{{ product.name }} - {{ product.price }}</h2>
			<p>Year: {{ product.year }}</p>
		</div>
		<RouterView></RouterView>
	</div>
</template>
