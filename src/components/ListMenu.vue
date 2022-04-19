<template>
		<ul>
            <li :key="item" v-for="item in list">
                {{item}}
            </li>
        </ul>
</template>

<script>
export default {
	name: "ListMenu",
	props: {
		list: String,
	},
};
</script>

<style lang="scss" scoped>
@import "../style/mixin.scss";
div{
    margin: 0;
}
ul {
	@include menu(column);
    padding: 0;
    margin: 0;
    li{
        font-size: 0.9rem;
        opacity: 0.8;
        margin: 2px 0;
    }
    :hover{
            scale: 2;
            opacity: 1;
    }
}
</style>
