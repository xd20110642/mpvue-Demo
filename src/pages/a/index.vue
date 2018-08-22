<template>
  <div class="a">
    <div class="my">
      <my></my>
    </div>
    <!--空白组件-->
    <Ceng></Ceng>
    <!--填写信息-->
    <div class="mess">
      <p class="text" @click="a">个人资料</p>
      <p class="text">我的优惠券</p>
    </div>
    <!--空白组件-->
    <Ceng></Ceng>
    <!--填写信息-->
    <div class="mess">
      <p class="text">常见问题</p>
      <p class="text">使用条框</p>
      <p class="text">常见问题</p>
      <p class="text">使用条框</p>
    </div>
    <!--空白组件-->
    <Ceng></Ceng>
    <div class="mess">
      <p class="text">常见问题</p>
    </div>

  </div>
</template>

<script>
  import my from "../../components/my/my.vue"
  import Ceng from "../../components/ceng/ceng";
    export default {
        name: "index",
        components:{
          Ceng,
          my
        },
      methods:{
          a(){
            wx.navigateTo({
              url:'../list/main',
              success(){
                console.log("跳转成功")
              }
            })
          }
      }
    }
</script>

<style scoped lang="scss">
  @import "../../commos/commos.scss";
    .a{
      width: 100%;
      .my{
        width: 100%;
      }
      .mess{
        width: 100%;
        .text{
          width: 100%;
          height: rpx(87);
          font-size: 16px;
          line-height:rpx(87);
          font-weight: bold;
          padding-left: 10px;
          @include border-1px-bottom(#ccc);
        }
      }
    }
</style>
