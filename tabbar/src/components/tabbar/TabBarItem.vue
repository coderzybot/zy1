<template>
  <div class="tab-bar-item" @click="itemClick">
    <div v-if="!isAtive"><slot  name="item-icon"></slot></div>
    <div v-else><slot name="item-icon-active"></slot></div>

    <div :style="activeStyle"><slot name="item-text">a</slot></div>
    <!--<img src="../../assets/img/shouye.png" alt=""/>-->
    <!--<div>首页</div>-->
  </div>
</template>

<script>
    export default {
        name: "TabBarItem",
        props:{
          path:String,
          activeColor:{
            type:String,
            default:'red'
          }
        },
        data(){
          return{
            //isAtive:true
          }
        },
      computed:{
        isAtive(){
          return this.$route.path.indexOf(this.path) !==-1
        },
        activeStyle(){
          return this.isAtive?{color:this.activeColor}:{}
          //通过props自定义 activeColor的颜色
        }
      },
      methods:{
        itemClick(){
          this.$router.replace(this.path)
        }
      }
    }
</script>

<style scoped>

  .tab-bar-item{
    flex:1;
    text-align: center;
    height:49px;
    font-size:14px;

  }
  .tab-bar-item img{
    width: 24px;
    height:24px;
    vertical-align:middle;
    margin-bottom: 2px;
  }
  .active{
    color:red;
  }
</style>
