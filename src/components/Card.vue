<script setup>
const props = defineProps({
	imageUrl: String,
	title: String,
	price: Number,
	isFavorite: Boolean,
	isAdded: Boolean,
	onClickAdd: Function,
	onClickFavorite: Function
})


</script>

<template>
	<div class="relative border border-slate-100 bg-white transition p-8 cursor-pointer rounded-3xl hover:-translate-y-2 hover:shadow-xl">
		<img @click="onClickFavorite" class="absolute top-8 left-8" :src="isFavorite ? '/like-2.svg' : '/like-1.svg'" alt="Like">
		<img :src="imageUrl" alt="sneaker">

		<p class="mt-2">{{ title }}</p>

		<div class="flex justify-between mt-5">
			<div class="flex flex-col">
				<span class="text-slate-400">Цена:</span>
				<b>{{ price }} руб.</b>
			</div>
			<img @click="onClickAdd" :src="isAdded ? '/checked.svg' : '/plus.svg'" alt="Plus">
		</div>
	</div>
</template>

<style scoped>

</style>