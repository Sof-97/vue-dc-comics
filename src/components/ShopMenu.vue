<template>
	<div>
		<h3>SHOP</h3>
		<ul>
			<li :key="item" v-for="item in menu">
				<span>{{ item }}</span>
			</li>
		</ul>
	</div>
</template>
<script>
export default {
	name: "ShopMenu",
	data() {
		return {
			menu: ["Shop DC", "Shop DC Collectibles"],
		};
	},
};
</script>

<style lang="scss">
@import "../style/mixin.scss";
h3{
    font-weight: bold;
}
ul{
	@include menu(column);
    padding: 0;
}
</style>
