<template>
	<div>
		<ul>
			<li :key="i" v-for="(item, i) in shop">
                <!-- TODO Risolvere url immagini <img  :src="`${item.img}`" alt=""> -->
                <p>{{item.name}}</p>
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
					img: "../assets/img/buy-comics-digital-comics.png",
				},
				{
					name: "dc merchandise",
					img: "../assets/img/buy-comics-merchandise.png",
				},
				{
					name: "subscription",
					img: "../assets/img/buy-comics-subscriptions.png",
				},
				{
					name: "comic shop locator",
					img: "../assets/img/buy-comics-shop-locator.png",
				},
				{
					name: "dc power visa",
					img: "../assets/img/buy-dc-power-visa.svg",
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
	li{
		color: white;
		text-transform: uppercase;
		margin: 0 15px;
	}
}
</style>
