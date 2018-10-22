<template>
<!-- 收藏食谱 -->
  <div class="collection">
    <!-- 未登录 -->
    <div class="login">
        <div class="img">
          <img src="../../../static/images/pic_on.png"/>
        </div>
        <span>登录后即可收藏喜欢的食谱</span>
        <!-- 登录 -->
        <div class="login_btn">
            <button open-type="getUserInfo" lang="zh_CN" @getuserinfo="onGotUserInfo">我的收藏</button>
        </div>
    </div>
    <!-- 登录之后 -->
    <!-- 头部 -->
    <div class='content'>
      <!-- 头部 -->
      <div class="header">
        <!-- 头像图片 -->
        <div class="head-img">
          <img src="//upload.jianshu.io/users/upload_avatars/8134145/f82e226c-8bdb-42c9-b5c8-7519ccb52564?imageMogr2/auto-orient/strip|imageView2/1/w/240/h/240"/>
        </div>
      <!-- 右侧内容 -->
        <div class="content">
      <!-- 用户名称 -->
        <div class="name">
            用户昵称
        </div>
        <!-- 收藏数量 -->
        <div class="colletion-number">
          收藏数量 0
        </div>
        </div>

      </div>

      <div class="content">
        <div class="collections">
    <i-swipeout  i-class="i-swipeout-demo-item" :actions="actions">
    <!-- 图片 -->
    <div class="img">
      <img  src="//img13.360buyimg.com/n7/jfs/t14311/328/1845717040/208534/37f7bc56/5a5cae15N0f2b3101.jpg!q70.dpg"/>
    </div>
    <div class="contents">
      <!-- 名称 -->
      <div class="name">
安格斯西冷1.5cm7分熟（林...
      </div>
      <!-- 作者 -->
      <div class="author">
宜居云厨房
      </div>
      <!-- 收藏数量 -->
      <div class="number">
1712收藏
      </div>
    </div>
    </i-swipeout>
  </div>
      </div>
    </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      actions: [
        {
          name: "喜欢",
          color: "#fff",
          fontsize: "20",
          width: 100,
          icon: "like",
          background: "#ed3f14"
        },
        {
          name: "返回",
          width: 100,
          color: "#80848f",
          fontsize: "20",
          icon: "undo"
        }
      ]
    };
  },
  computed: {},
  methods: {
    onGotUserInfo(e) {
      console.log(e);
      console.log(e.mp.detail.userInfo);
    }
  }
};
</script>

<style lang='less' scoped>
.login {
  position: fixed;
  top: 0;
  left: 0;
  display: none;
  width: 100%;
  height: 100%;
  background: #f7f7f7;
  .img {
    width: 100%;
    text-align: center;
    margin-top: 151px;
    img {
      width: 90px;
      height: 90px;
      text-align: center;
    }
  }
  span {
    font-size: 14px;
    width: 100%;
    margin-top: 10px;
    display: block;
    color: #898989;
    text-align: center;
  }

  .login_btn {
    margin-top: 84px;
    padding: 0 60px;
    button {
      background: #f5a623;
      border-radius: 20px;
      color: #010101;
    }
  }
}
.collection {
  .header {
    height: 120px;
    display: flex;
    width: 100%;
    border-bottom: 10px solid #f7f7f7;
    .head-img {
      width: 90px;
      margin: 15px;
      border-radius: 50%;
      overflow: hidden;
      height: 90px;
      img {
        width: 90px;
        height: 90px;
      }
    }
    .content {
      .collections {
        display: flex;
        padding: 15px 0;

        .img {
          padding-left: 15px;
          border-radius: 3px;
          width: 115px;
          overflow: hidden;
          height: 100px;
          img {
            width: 100%;
          }
        }
        .contents {
          padding-bottom: 15px;
          padding-left: 15px;
          padding-top: 15px;

          border-bottom: 0.5px solid #ccc;
          flex: 1;
          .name {
            font-size: 16px;
            color: #4a4a4a;
          }
          .author {
            font-size: 14px;
            color: #898989;
            margin-top: 10px;
            letter-spacing: -0.34px;
          }
          .number {
            margin-top: 10px;

            font-size: 14px;
            color: #898989;
          }
        }
      }

      flex: 1;
      .name {
        font-size: 16px;
        color: #4a4a4a;
        margin-top: 30px;
      }
      .colletion-number {
        font-size: 14px;
        color: #898989;
        margin-top: 10px;
      }
    }
  }
}
</style>
