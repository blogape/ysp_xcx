<template>
<!-- 食谱软文 -->
<div class="articles">
  <!-- 左侧图片 -->
  <div class="img">
    <img src="https://recipes.oss-cn-shenzhen.aliyuncs.com/article111.jpg"/>
  </div>
  <!-- 右侧内容 -->
  <div class="content">
    <!-- 名称 -->
    <div class="name">
      好问豆答：和面与发面的技巧…
    </div>
    <!-- 作者 -->
    <div class="author">
    水蓝冰清 <span>4天前</span>
    </div>
    <!-- 描述 -->
    <div class="describle">
      作为北方人，平常的主食就是面食…
    </div>
  </div>
</div>
</template>

<script>
export default {};
</script>

<style lang='less' scoped>
.articles {
  width: 100%;
  display: flex;
  .img {
    padding-left: 15px;
    width: 119px;
    height: 100px;
    overflow: hidden;
    img {
      width: 100%;
    }
  }
  .content {
    font-size: 16px;
    color: #4a4a4a;
    padding-left: 15px;
    border-bottom: 0.5px solid #ccc;
    padding-bottom: 30px;
    .name {
      height: 30px;
      line-height: 30px;
    }
    .author {
      font-size: 14px;
      color: #898989;
      span{
        margin-left: 5px;
      }
    }
    .describle{
      font-size: 14px;
      color: #898989;
      margin-top: 10px;
      line-height: 20px;
    }
  }
}
</style>
