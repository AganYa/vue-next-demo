<template>
  <div class="contanier">
    <div class="header_contanier">
      <a class="category" href="#"></a>
      <div class="search">
        <input class="input_item" placeholder="搜索" type="text" />
      </div>
      <a class="login" href="#">登录</a>
    </div>

    <!-- 轮播图 -->
    <div class="banner">
      <Swiper v-if="bannerList.length > 0">
        <Slide :key="index" v-for="(item,index) in bannerList">
          <img :src="item" />
        </Slide>
      </Swiper>
      <!-- <img alt src="../assets/image/banner_01.jpg" srcset /> -->
    </div>

    <!-- 广告 -->
    <div class="ad">
      <a href="#">
        <img alt src="../assets/image/ad_01.png" />
      </a>
      <a href="#">
        <img alt src="../assets/image/ad_02.png" />
      </a>
      <a href="#">
        <img alt src="../assets/image/ad_03.png" />
      </a>
    </div>

    <!-- 导航 -->
    <nav>
      <a :key="index" href="#" v-for="(item ,index) in navIconList">
        <img :src="item.url" />
        <div>{{item.iconName}}</div>
      </a>
    </nav>
    <nav>
      <a :key="index" href="#" v-for="(item ,index) in navIconList">
        <img :src="item.url" />
        <div>{{item.iconName}}</div>
      </a>
    </nav>
    <nav>
      <a :key="index" href="#" v-for="(item ,index) in navIconList">
        <img :src="item.url" />
        <div>{{item.iconName}}</div>
      </a>
    </nav>
    <nav>
      <a :key="index" href="#" v-for="(item ,index) in navIconList">
        <img :src="item.url" />
        <div>{{item.iconName}}</div>
      </a>
    </nav>

    <TabBar></TabBar>
  </div>
</template>

<script>
import { Swiper, Slide } from 'vue-swiper-component';
import TabBar from '../components/TabBar.vue';
const NAV_ICON_LIST = [
  {
    url: require('../assets/image/nav_icon_01.png'),
    iconName: '天天低价'
  },
  {
    url: require('../assets/image/nav_icon_02.png'),
    iconName: '苏宁超市'
  },
  {
    url: require('../assets/image/nav_icon_03.png'),
    iconName: '苏宁拼购'
  },
  {
    url: require('../assets/image/nav_icon_04.png'),
    iconName: '5G手机'
  },
  {
    url: require('../assets/image/nav_icon_05.png'),
    iconName: '苏宁家电'
  },
  {
    url: require('../assets/image/nav_icon_06.png'),
    iconName: '免费水果'
  },
  {
    url: require('../assets/image/nav_icon_07.png'),
    iconName: '赚钱消消乐'
  },
  {
    url: require('../assets/image/nav_icon_08.png'),
    iconName: '签到有礼'
  },
  {
    url: require('../assets/image/nav_icon_09.png'),
    iconName: '领卷中心'
  },
  {
    url: require('../assets/image/nav_icon_10.png'),
    iconName: '更过频道'
  }
];
const BANNER_LIST = [
  require('../assets/image/banner_01.jpg'),
  require('../assets/image/banner_02.jpg'),
  require('../assets/image/banner_03.png'),
  require('../assets/image/banner_04.png'),
  require('../assets/image/banner_05.png'),
  require('../assets/image/banner_06.png')
];
export default {
  name: 'home',
  components: {
    Swiper,
    Slide,
    TabBar
  },
  data() {
    return {
      navIconList: NAV_ICON_LIST,
      bannerList: BANNER_LIST
    };
  }
};
</script>
<style lang="less" scoped>
@baseFontSize: 50;
.contanier {
  // position: relative;
  // z-index: 33;
  .header_contanier {
    display: flex;
    position: fixed;
    top: 0;
    left: 50%;
    z-index: 2;
    transform: translateX(-50%);
    height: 88rem / @baseFontSize;
    width: 15rem;
    background: #ffc001;
  }
  .category {
    width: 44rem / @baseFontSize;
    height: 70rem / @baseFontSize;
    margin: 11rem / @baseFontSize 25rem / @baseFontSize 7rem / @baseFontSize
      25rem / @baseFontSize;
    background: url('../assets/image/category.png') no-repeat;
    background-size: 44rem / @baseFontSize 70rem / @baseFontSize;
  }
  .search {
    flex: 1;

    input {
      outline: none;
      width: calc(100% - 100rem / @baseFontSize);
      height: 66rem / @baseFontSize;
      font-size: 25rem / @baseFontSize;
      padding: 0 50rem / @baseFontSize;
      border: 0;
      border-radius: 33rem / @baseFontSize;
      color: #757575;
      background-color: #fff2cc;
    }
  }
  .login {
    width: 75rem / @baseFontSize;
    height: 70rem / @baseFontSize;
    margin: 10rem / @baseFontSize;
    font-size: 25rem / @baseFontSize;
    text-align: center;
    line-height: 70rem / @baseFontSize;
    color: #fff;
  }

  .banner {
    width: 750rem / @baseFontSize;
    height: 368rem / @baseFontSize;
    margin-top: 88rem / @baseFontSize;
    img {
      width: 100%;
      height: 100%;
    }
  }

  .ad {
    display: flex;
    a {
      flex: 1;
      img {
        width: 100%;
      }
    }
  }

  nav {
    width: 750rem / @baseFontSize;
    a {
      float: left;
      width: 150rem / @baseFontSize;
      height: 140rem / @baseFontSize;
      img {
        display: block;
        width: 82rem / @baseFontSize;
        height: 82rem / @baseFontSize;
        margin: 10rem / @baseFontSize auto 0;
      }

      div {
        margin-top: 5rem / @baseFontSize;
        font-size: 25rem / @baseFontSize;
        text-align: center;
        color: #333;
      }
    }
  }
}
</style>
