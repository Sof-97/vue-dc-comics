<template>
	<div>
		<ul>
			<li
				@click="toggle(i)"
				:key="i"
				v-for="(item, i) in mainMenu"
				:class="selected == i ? 'active' : ''"
			>
				{{ item }}
			</li>
		</ul>
	</div>
</template>

<script>
export default {
	name: "HeaderMenu",
	data() {
		return {
			mainMenu: [
				"characters",
				"comics",
				"movies",
				"tv",
				"games",
				"collectibles",
				"videos",
				"fans",
				"news",
				"shop",
			],
			selected: 0,
		};
	},
	methods: {
		toggle(i) {
			this.selected = i;
		},
	},
};
</script>

<style lang="scss" scoped>
@import "../style/mixin.scss";
@import "../style/variables.scss";
ul {
	@include menu(row);
	li {
		padding: 20px;
	}
	.active {
		color: $blue;
	}
	.active::after {
		content: "";
		display: block;
		position: relative;
		top: 25px;
		height: 4px;
		background-color: $blue;
	}
}
</style>
