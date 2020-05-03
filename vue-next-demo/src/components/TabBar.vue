<template>
  <div>
    <van-tabbar v-model="active">
      <van-tabbar-item icon="like-o">猜你喜欢</van-tabbar-item>
      <van-tabbar-item icon="search">分类</van-tabbar-item>
      <van-tabbar-item icon="description">必抢清单</van-tabbar-item>
      <van-tabbar-item icon="cart-o">购物车</van-tabbar-item>
      <van-tabbar-item icon="user-o">我的易购</van-tabbar-item>
    </van-tabbar>
  </div>
</template>

<script>
import { Tabbar } from 'vant';
import { TabbarItem } from 'vant';
export default {
  components: {
    'van-tabbar': Tabbar,
    'van-tabbar-item': TabbarItem
  },
  data() {
    return {
      active: 0
    };
  }
};
</script>

<style>
</style>