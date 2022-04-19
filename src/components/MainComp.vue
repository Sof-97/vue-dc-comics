<template>
	<div class="container">
		<div class="jumbo"></div>
		<div>
			<p class="series">current series</p>
			<div class="comics">
				<ComicComp :items="comicData" />
			</div>
			<div class="more">
				<span>load more</span>
			</div>
		</div>
	</div>
</template>

<script>
import ComicComp from "../components/ComicComp.vue";
import data from "../components/dc-comics.json";

export default {
	name: "MainComp",
	components: {
		ComicComp,
	},
	data() {
		return {
			comicData: data,
		};
	},
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
div.container {
	background-color: #333;
	color: white;
	.jumbo {
		background-image: url("../assets/img/jumbotron.jpg");
		height: 300px;
		background-position-x: center;
		background-size: cover;
	}
	div {
		position: relative;
		p {
			margin: 0;
		}
		.series {
			position: absolute;
			top: -20px;
			left: 15%;
			padding: 10px 20px;
			display: inline-block;
			text-transform: uppercase;
			font-weight: bold;
			background-color: $blue;
		}
		.more{
      display: flex;
      justify-content: center;
      span{
			text-transform: uppercase;
			font-weight: bold;
			padding: 15px 50px;
			background-color: $blue;
			margin-bottom: 30px;
		}}
		.comics {
			padding: 50px;
		}
	}
}
</style>
