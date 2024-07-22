<script setup>
import { useRoute, useRouter, RouterView } from "vue-router";
import products from "../data/products.json";

const route = useRoute();
const router = useRouter();
const productId = parseInt(route.params.id);
const product = products.find((product) => product.id === productId);

function showOwner() {
	router.push({ name: "owner", params: { id: productId } });
}
</script>

<template>
	<div>
		<h1>Product</h1>
		<div>
			<h2>{{ product.name }} - {{ product.price }}</h2>
			<p>Year: {{ product.year }}</p>
		</div>
		<button @click="showOwner()">Show Owner</button>
		<RouterView />
	</div>
</template>
