<template>
	<div id="app">
		<header>
			<img src="./assets/img/dc-logo.png" alt="Logo DC Comics">
			<HeaderMenu/>
		</header>
		<MainComp />
		<BeforeFooter/>
		<FooterComp />
	</div>
</template>

<script>
import HeaderMenu from "./components/HeaderMenu.vue";
import MainComp from "./components/MainComp.vue";
import BeforeFooter from "./components/BeforeFooter.vue";
import FooterComp from "./components/FooterComp.vue";

export default {
	name: "App",
	components: {
		HeaderMenu,
		MainComp,
		BeforeFooter,
		FooterComp,
	},
	data() {
		return {
		
		};
	},
};
</script>

<style lang="scss">

@import './style/variables.scss';

#app {
	font-family: helvetica;
	header{
		max-width: 90%;
		padding: 15px 0 ;
		display: flex;
		justify-content: space-around;
		text-transform: uppercase;
		font-weight: bold;
		color: $grey;
	}
}
</style>
