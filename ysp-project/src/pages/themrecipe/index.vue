<template>
<!-- 主题食谱 -->
  <div class="themrecipe">
    <!-- 主题食谱标题 -->
    <div class="title">
        绝不失手的中秋大餐，上桌就抢光！
    </div>
    <!-- 食谱数量 -->
    <div class="number">
      -12道菜谱-
    </div>
    <!-- 主题内容 -->
    <div class="content">
        <ul>
          <li>
              <articles></articles>
          </li>
          <li>
              <articles></articles>

          </li>
          <li>
              <articles></articles>

          </li>
        </ul>
    </div>
  </div>
</template>

<script>
import articles from "@/components/articles/";
export default {
  components:{
    articles
  }
}
</script>

<style lang='less' scoped>
.themrecipe{
  .title{
    height: 45px;
padding-top: 10px;
    line-height: 45px;
    text-align: center;
    font-size: 18px;
    color: #4A4A4A;
  }
  .number{
    font-size: 14px;
    text-align: center;
    padding: 15px 0;
    color: #898989;
  }
  .content{
    ul{
      li{
        margin-top: 10px;
      }
    }
  }
}
</style>
