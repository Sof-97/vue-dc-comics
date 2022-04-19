<template>
	<div class="box">
		<div>
			<h3>DC COMICS</h3>
			<ListMenu
				:list="comics"
			/>
			<h3>SHOP</h3>
			<ListMenu :list="shop"/>
		</div>
        <div>
            <h3>DC</h3>
		<ListMenu :list="terms" />
        </div>
		
        <div>
            <h3>SITES</h3>
		<ListMenu :list="dcSites"/>
        </div>
		
	</div>
</template>

<script>
import ListMenu from "./ListMenu.vue";

export default {
	name: "MenuFooter",
	components: {
		ListMenu,
	},
	data() {
		return {
			comics: [
				"Charachters",
				"Comics",
				"Movies",
				"TV",
				"Games",
				"Videos",
				"News",
			],
			shop: ["Shop DC", "Shop DC Collectibles"],
			terms: [
				"Terms Of Use",
				"Privacy policy (New)",
				"Ad Choices",
				"Advertising",
				"Jobs",
				"Subscriptions",
				"Talent Workshops",
				"CPSC Certificates",
				"Ratings",
				"Shop Help",
				"Contact Us",
			],
			dcSites: [
				"DC",
				"MAD Magazine",
				"DC Kids",
				"DC Universe",
				"DC Power Visa",
			],
		};
	},
};
</script>
<style lang="scss" scoped>
@import "../style/mixin.scss";
h3{
    font-weight: bold;
    margin: 10px 0;
}
.box {
	@include menu(row);
    padding: 30px 0;
}
div {
	color: white;
    margin: 0 10px;
}
</style>
