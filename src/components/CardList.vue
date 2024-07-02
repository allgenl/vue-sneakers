<script setup>
import Card from "@/components/Card.vue";

const onClickAdd = () => {
}
const onClickFavorite = () => {

}
</script>

<template>
	<div class="grid grid-cols-4 gap-5">
		<Card image-url="/sneakers/sneakers-1.jpg"
		      title="Мужские кроссовки Nike"
		      :price="12999"
					:is-favorite="true"
		      :is-added="true"
		      :on-click-add="onClickAdd"
		      :on-click-favorite="onClickFavorite"
		/>
		<Card image-url="/sneakers/sneakers-2.jpg"
		      title="Мужские кроссовки Adidas"
		      :price="14999"
					:is-favorite="false"
		      :is-added="false"
		      :on-click-add="onClickAdd"
		      :on-click-favorite="onClickFavorite"
		/>
	</div>
</template>

<style scoped>

</style>