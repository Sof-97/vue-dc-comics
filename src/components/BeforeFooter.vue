<template>
	<div>
		<ul>
			<li :key="i" v-for="(item, i) in shop">
				<img
					style="width: 100px"
					:src="require(`../assets/img/${item.img}`)"
					alt=""
				/>
				<p>{{ item.name }}</p>
			</li>
		</ul>
	</div>
</template>

<script>
export default {
	name: "BeforeFooter",
	data() {
		return {
			shop: [
				{
					name: "digital comics",
					img: "buy-comics-digital-comics.png",
				},
				{
					name: "dc merchandise",
					img: "buy-comics-merchandise.png",
				},
				{
					name: "subscription",
					img: "buy-comics-subscriptions.png",
				},
				{
					name: "comic shop locator",
					img: "buy-comics-shop-locator.png",
				},
				{
					name: "dc power visa",
					img: "buy-dc-power-visa.svg",
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
@import "../style/mixin.scss";
@import "../style/variables.scss";
ul {
	margin: 0;
	display: flex;
	justify-content: center;
	background-color: $blue;
	@include menu(row);
	padding: 20px 0;
	li {
		display: flex;
		color: white;
		text-transform: uppercase;
		margin: 0 15px;
		align-items: center;
		img{
			width: 30px;
			margin-right: 10px;
		}
	}
}
</style>
