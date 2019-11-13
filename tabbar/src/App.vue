<template>
  <div id="app">
  <tab-bar>
    <tab-bar-item path="/home" activeColor="blue">
      <img slot="item-icon" src="./assets/img/shouye.png"/>
      <img slot="item-icon-active" src="./assets/img/sy-d.png"/>
      <div slot="item-text">首页</div>
    </tab-bar-item >
    <tab-bar-item path="/category" activeColor="blue">
      <img slot="item-icon" src="./assets/img/fenle.png"/>
      <img slot="item-icon-active" src="./assets/img/fl-d.png"/>
      <div slot="item-text">分类</div>
    </tab-bar-item>
    <tab-bar-item path="/cart" activeColor="blue">
      <img slot="item-icon" src="./assets/img/gouwuc.png"/>
      <img slot="item-icon-active" src="./assets/img/gwc-d.png"/>
      <div slot="item-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item path="profile" activeColor="blue">
      <img slot="item-icon" src="./assets/img/wd.png"/>
      <img slot="item-icon-active" src="./assets/img/wd-d.png"/>
      <div slot="item-text">我的</div>
    </tab-bar-item>
  </tab-bar>
    <router-view></router-view>
  </div>
</template>

<script>
  import TabBar from './components/tabbar/TabBar'
  import TabBarItem from './components/tabbar/TabBarItem'
  export default {
    name: 'App',
    components:{
      TabBar,
      TabBarItem
    }
  }
  </script>

<style>
  @import "./assets/css/base.css";

</style>
