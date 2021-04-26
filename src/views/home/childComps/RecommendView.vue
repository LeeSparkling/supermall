<template>
    <div class="recommend">
        <div class="item" v-for="item in recommends">
            <a :href="item.link">
                <img :src="item.image">
                <div class="recommend-title">{{item.title}}</div>
            </a>
        </div>
    </div>
</template>

<script>
  export default {
    name: "RecmmendView",
    props:{
      recommends:{
        type:Array,
        default() {
          return [];
        }
      }
    }
  }
</script>

<style scoped>
    .recommend{
        display: flex;
        width: 100%;
        justify-content:space-around;
        padding: 15px 0 20px;
        border-bottom: 8px solid #eee;
    }
    .recommend-title{
        text-align: center;
        font-size: 12px;
    }
    .item img{
        width: 65px;
        height: 65px;
        margin-bottom: 5px;
    }
</style>