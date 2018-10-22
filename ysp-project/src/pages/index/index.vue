<template>
<!-- 首页 -->
  <div class="home">
    <!-- bannner图 -->
    <div class="banner">
    <swiper :indicator-dots="indicatorDots"
      :autoplay="autoplay"  :interval="interval" :duration="duration" indicatorDots='true'  circular='true'>
      <block v-for='(item,key) in imgUrls' :key='key'>
       <swiper-item>
      <image :src="item" class="slide-image" width="355" height="150"/>
    </swiper-item>
  </block>
</swiper>
    </div>
    <!-- 选项 -->
    <div class="content">
    <i-tabs :current="current" @change="handleChange" color="#F5A623" >
      <!-- 热门食谱 -->
    <i-tab key="tab1" title="热门食谱">
    </i-tab>
    <!-- 主题食谱 -->
    <i-tab key="tab2" title="主题食谱">主题食谱</i-tab>
      <!-- 美食知识 -->
    <i-tab key="tab3" title="美食知识">美食知识</i-tab>
    </i-tabs>
    <!-- 热门食谱内容 -->
    <div class="hotrecipe" v-if="current=='tab1'">
        <ul>
          <li>
              <goods></goods>
          </li>
          <li>
          <goods></goods>
          </li>
          <li></li>
        </ul>
    </div>
    <!-- 主题食谱 -->
    <div class="themrecipe" v-if="current=='tab2'">
      <ul>
        <li>
          <themRecipe></themRecipe>
        </li>
      </ul>
    </div>
    <!-- 食谱软文 -->
    <div class="recipearticle" v-if="current=='tab3'">
      <ul>
        <li>
      <articles></articles>
        </li>
         <li>
      <articles></articles>
        </li>
      </ul>
    </div>
    </div>
    <!-- <a href="/pages/recipedetail/main">食谱详情</a> -->
  </div>
</template>

<script>
import card from "@/components/card";
import goods from "@/components/goods/";
import themRecipe from "@/components/theme/";
import articles from "@/components/articles/";
export default {
  data() {
    return {
      imgUrls: [
        "http://img02.tooopen.com/images/20150928/tooopen_sy_143912755726.jpg",
        "http://img06.tooopen.com/images/20160818/tooopen_sy_175866434296.jpg",
        "http://img06.tooopen.com/images/20160818/tooopen_sy_175833047715.jpg"
      ],
      userInfo: {},
      indicatorDots: false,
      autoplay: true,
      interval: 5000,
      duration: 1000,
      current: "tab2"
      // current_scroll: 'tab1'
    };
  },

  components: {
    articles,
    card,
    goods,
    themRecipe
  },

  methods: {
    // 选项卡
    handleChange(detail) {
      this.current = detail.target.key;
    },

    handleChangeScroll() {
      // console.log(e);
      //  this.current='tabs'
    },

    bindViewTap() {
      const url = "../logs/main";
      wx.navigateTo({ url });
    },
    getUserInfo() {
      // 调用登录接口
      wx.login({
        success: () => {
          wx.getUserInfo({
            success: res => {
              this.userInfo = res.userInfo;
            }
          });
        }
      });
    }
  },

  created() {
    // 调用应用实例的方法获取全局数据
    this.getUserInfo();
  }
};
</script>

<style scoped lang='less'>
.home {
  .banner {
    overflow: hidden;
    image {
      width: 100%;
    }
  }
  .content {
    height: auto;
    background-color: #fff;
    overflow: hidden;
    .hotrecipe {
      padding: 0 5px;
      overflow: hidden;
      height: auto;
      background-color: #f7f7f7;
      ul {
        li:nth-child(2n) {
          padding-left: 3px;
        }
        li:nth-child(2n + 1) {
          padding-right: 3px;
        }
        li {
          float: left;
          overflow: hidden;
          height: auto;
          width: 50%;
          margin-top: 5px;
          box-sizing: border-box;
          position: relative;
        }
      }
    }
    .themrecipe {
      ul {
        li {
          position: relative;
          padding: 15px;
        }
      }
    }
    .recipearticle {
      ul {
        li {
          margin-top: 10px;
        }
        li:last-child{
          .content{
            border-bottom: none;
          }
        }
      }
    }
  }
}
</style>
