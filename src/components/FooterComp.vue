<template>
  <footer>
    <MenuFooter/>
    <img src="../assets/img/dc-logo-bg.png" alt="">
  </footer>
</template>

<script>
import MenuFooter from "./MenuFooter.vue";
export default {
	name: "FooterComp",
  components: {
    MenuFooter,
  }
};
</script>

<style lang="scss" scoped>
  footer{
    height:300px;
    background-image: url(../assets/img/footer-bg.jpg);
    display: flex;
    justify-content: space-around;
  }
</style>
