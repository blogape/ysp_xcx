<template>
<!-- 首页 -->
  <div class="home">
    <!-- bannner图 -->
    <div class="banner">
    <swiper :indicator-dots="indicatorDots"
      :autoplay="autoplay"  :interval="interval" :duration="duration">
      <block v-for='(item,key) in imgUrls' :key='key'>
       <swiper-item>
      <image :src="item" class="slide-image" width="355" height="150"/>
    </swiper-item>
  </block>
</swiper>
    </div>
  </div>
</template>

<script>
import card from "@/components/card";
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
      autoplay: false,
      interval: 5000,
      duration: 1000
    };
  },

  components: {
    card
  },

  methods: {
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
.div {
  p {
    font-size: 144rpx;
  }
}
</style>
