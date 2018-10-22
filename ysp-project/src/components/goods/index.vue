<template>
<!-- 商品 -->
<a class="goods">
<div class="similar-product">
  <div class="similar-posre">
    <!-- 图片 -->
     <img  src="//img11.360buyimg.com/n7/jfs/t22912/82/2590779211/130844/464eb169/5b87536bNb250f0de.jpg!q70.dpg" class="j_rec_goods_pic opa1 ll_fadeIn" loaded="1" >
     </div>
     <!-- 名称 -->
     <span class="similar-product-text">
        云南特产美和云腿肉要吃饭了吗啊啊啊
      </span>
      <!-- 收藏数量 -->
      <p class="collect-number">227收藏</p>
      </div>
</a>
</template>

<script>
export default {};
</script>

<style lang='less' scoped>
.goods {
  width: 100%;
  display: inline-block;
  .similar-product {
    width: 100%;
    background-color: #fff;
    img {
      display: block;
      width: 100%;
    }
    .similar-posre {
      display: block;
      width: 100%;
      position: relative;
    }
    .similar-product-text {
      box-sizing: border-box;
      height: 15px;
      font-size: 16px;
      overflow: hidden;
      text-overflow: ellipsis;
      display: -webkit-box;
      -webkit-line-clamp: 1;
      -webkit-box-orient: vertical;
      word-break: break-word;
      color: #232326;
      margin-top: 5px;
      line-height: 16px;
      margin-bottom: 3px;
      padding: 0 4px;
    }
    .collect-number {
      font-size: 12px;
      color: #898989;
      height: 25px;
      line-height: 25px;
      padding: 0 8rpx;
    }
  }
}
</style>
