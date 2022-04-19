<template>
	<div class="container">
		<p>Sign-up now!</p>
		<div>
			<span>follow us</span>
            <img src="../assets/img/footer-facebook.png" alt="Logo Social fb">
            <img src="../assets/img/footer-twitter.png" alt="Logo Social tw">
            <img src="../assets/img/footer-youtube.png" alt="Logo Social yt">
            <img src="../assets/img/footer-pinterest.png" alt="Logo Social pt">
            <img src="../assets/img/footer-periscope.png" alt="Logo Social pr">
		</div>
	</div>
</template>

<script>
export default {
	name: "SocialComp",
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

div.container {
	background-color: $grey;
	display: flex;
	justify-content: space-around;
	> p {
		color: white;
		text-transform: uppercase;
		border: 2px solid $blue;
		padding: 10px;
	}
	div {
        display: flex;
        flex-direction: row;
        align-items: center;
		span {
			color: $blue;
			text-transform: uppercase;
			font-weight: bold;
			font-size: 1.3rem;
            margin-right: 15px;
		}
        img{
            width: 40px;
            height: 40px;
            margin-right: 5px;
        }
	}
}
</style>
