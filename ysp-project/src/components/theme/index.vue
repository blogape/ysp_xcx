<template>
<!-- 主题食谱 -->
<a class="them" href="/pages/themrecipe/main">
  <!-- 图片 -->
<div class="img">
<img src="https://ejy.oss-cn-shanghai.aliyuncs.com/f5bf6c4950af438aa528871da0f2150a.jpeg"/>
</div>
<!-- 遮层 -->
<i class="bg"></i>
<div class="text">
  <p class="name">绝不失手的中秋大餐，上桌就抢光！</p>
  <p class="describle">12道菜谱</p>
</div>
</a>
</template>

<script>
export default {

}
</script>

<style lang='less' scoped>
.them{
  position: relative;
  height: 182px;
  border-radius: 3px;
  overflow: hidden;
  .img{
    width: 100%;
    top:0;
    left:0;
    position: absolute;
    img{
      width: 100%;
    }
  }
  .bg{
     width: 100%;
    top:0;
      height: 182px;
    left:0;
    z-index:99;
    position: absolute;
    background-color: rgba(0,0,0,0.3);
  }
  .text{
    z-index: 9999;
    color: #fff;
    position: absolute;
    width: 100%;
    height: 182px;
    .name{
      margin-top: 58px;
      text-align: center;
      padding: 0 30px;
      font-size:18px;
    }
    .describle{
      font-size: 14px;
      text-align: center;
      margin-top: 36px;
      color:#fff;
    }
  }
}
</style>
