<template>
  <div id = "cart">
    <nav-bar class = "cart-bar">
      <div slot="center">购物车</div>
    </nav-bar>
  </div>
</template>

<script>
  import NavBar from "../../components/common/navbar/NavBar"
  export default {
    name: "Cart",
    components:{
      NavBar
    }
  }
</script>

<style scoped>
  .cart-bar{
    background-color: #ff8198;
    color: #fff;
  }
</style>
