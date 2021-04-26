<template>
  <div id = "category">
    <nav-bar class = "category-bar">
      <div slot="center">分类</div>
    </nav-bar>
  </div>
</template>

<script>
  import NavBar from "../../components/common/navbar/NavBar"
  export default {
    name: "Category",
    components:{
      NavBar
    }
  }
</script>

<style scoped>
  .category-bar{
    background-color: #ff8198;
    color: #fff;
  }
</style>
