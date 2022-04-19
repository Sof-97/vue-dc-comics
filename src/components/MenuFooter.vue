<template>
	<div>
		<div>
			<ComicsMenu />
			<ShopMenu />
		</div>
		<TermsMenu />
		<SitesMenu />
	</div>
</template>

<script>
import ShopMenu from "./ShopMenu.vue";
import TermsMenu from "./TermsMenu.vue";
import SitesMenu from "./SitesMenu.vue";
import ComicsMenu from "./ComicsMenu.vue";

export default {
	name: "MenuFooter",
	components: {
		ComicsMenu,
		ShopMenu,
		TermsMenu,
		SitesMenu,
	},
};
</script>
<style lang="scss" scoped>
@import "../style/mixin.scss";

div {
	color: white;
}
</style>
