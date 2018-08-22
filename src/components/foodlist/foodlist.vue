<template>
    <div class="foodlist">
      <div class="left">
        <img src="http://placehold.it/100x100" alt="">
      </div>
      <div class="right">
        <div class="title">
          店铺名称:{{title}}
        </div>
        <div class="mess">
          <p class="phone">电话:18121831901</p>
          <p class="add">地址：成都高新区</p>
          <p class="time">营业时间:地球不爆炸 我们不休息</p>
        </div>
      </div>
      <div class="start">
        ⭐⭐⭐⭐⭐
      </div>
    </div>
</template>

<script>
    export default {
        name: "foodlist",
      props:{
          title:{
            type:String,
            default:'韩国泡菜'
          }
      }
    }
</script>

<style scoped lang="scss">
  @import "../../commos/commos.scss";
    .foodlist{
      position: relative;
      width: 90%;
      display: flex;
      margin: auto;
      margin-top: 10px;
      padding: 10px;
      @include border-1px-bottom(#ccc);
      .left{
        width: 100px;
        flex: 0 0 100px;
        img{
          width: 100px;
          height: 100px;
        }
      }
      .right{
        flex: 1;
        margin-left: rpx(5);
        .title{
          font-size: 16px;
          font-weight: bold;
        }
        .mess{
          color: #ccc;
          .phone,.add,.time{
            font-size: 14px;
            margin-top: rpx(10);
          }
        }
      }
      .start{
        box-sizing: border-box;
        width: 120px;
        position: absolute;
        right: 0;
        top: 0;
      }
    }
</style>
