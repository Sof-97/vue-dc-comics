<template>
	<ul>
		<li :key="item" v-for="item in items">
			<div>
				<img :src="`${item.thumb}`" alt="" />
                <p>{{item.series}}</p>
			</div>
		</li>
	</ul>
</template>
<script>
export default {
	name: "ComicComp",
	props: {
		items: Array,
	},
};
</script>

<style lang="scss" scoped>
@import "../style/mixin.scss";
ul {
    padding: 0;
    margin: 0;
	@include menu(row);
	display: flex;
	flex-wrap: wrap;
    justify-content: center;
	li {
        text-align: center;
        margin-top: 15px;
        width: calc(100%/6 - 5px);
        img{
            width: 200px;
        height: 200px; 
        object-fit: cover;
        object-position: 50% 20%;
        }
	}
}
</style>
