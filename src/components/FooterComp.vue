<template>
	<footer>
		<div>
			<MenuFooter />
			<div class="logo">
      </div>
		</div>
    <SocialComp />
	</footer>
</template>

<script>
import MenuFooter from "./MenuFooter.vue";
import SocialComp from "./SocialComp.vue"
export default {
	name: "FooterComp",
	components: {
		MenuFooter,
    SocialComp,
	},
};
</script>

<style lang="scss" scoped>
footer {
  > div{
    width: 100%;
    display: flex;
    justify-content: space-around;
  }
	background-image: url(../assets/img/footer-bg.jpg);
	div.logo{
		width: 40%;
		background-repeat: no-repeat;
		background-size: cover;
		background-position-y: 40%;
		background-image: url(../assets/img/dc-logo-bg.png);
	}
}
</style>
