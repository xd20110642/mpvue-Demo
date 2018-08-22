<template>
  <div class="index-nav">
    <div class="nav-item" @click="a">
      <img src="../../assets/icons/grid-01(1).png" alt="">
      <span>美食</span>
    </div>
    <div @click="a" class="nav-item">
      <img src="../../assets/icons/grid-02.png" alt="">
      <span>美食</span>
    </div>

    <div @click="a" class="nav-item">
      <img src="../../assets/icons/grid-03.png" alt="">
      <span>美食123</span>
    </div>
    <div @click="a" class="nav-item">
      <img src="../../assets/icons/grid-04.png" alt="">
      <span>美食</span>
    </div>
    <div @click="a" class="nav-item">
      <img src="../../assets/icons/grid-05.png" alt="">
      <span>美食</span>
    </div>
    <div @click="a" class="nav-item">
      <img src="../../assets/icons/grid-06.png" alt="">
      <span>美食</span>
    </div>
    <div @click="a" class="nav-item">
      <img src="../../assets/icons/grid-01(1).png" alt="">
      <span>美食</span>
    </div>
    <div @click="a" class="nav-item">
      <img src="../../assets/icons/grid-07.png" alt="">
      <span>美食</span>
    </div>
    <div @click="a" class="nav-item">
      <img src="../../assets/icons/grid-07.png" alt="">
      <span>美食</span>
    </div>

  </div>
</template>

<script>
    export default {
        name: "meun",
      methods:{
          a(){
          wx.navigateTo({
            url:'../../pages/list/main',
            success(){
              console.log("跳转成功")
            },
            fail(err){
              console.log(err)
            }
          })
            console.log(1)
          }
      }
    }
</script>

<style scoped lang="scss">
  @import "../../commos/commos.scss";

    .index-nav{
      width: 110%;
      display: flex;
      flex-wrap: wrap;//换行
      .nav-item:nth-of-type(3n+1){
        border-right: 0 none;
      }
      .nav-item{
        box-sizing: border-box;
        width: 30%;
        height: rpx(200);
        @include border-1px-bottom(#ccc);
        @include border-1px-right(#ccc);
        display: flex;
        flex-direction: column;//设置主轴
        align-items: center;//设置次轴的对齐方式
        img{
          width:rpx(80);
          height: rpx(80);
          margin-top: rpx(10);

        }
        span{
          /*display: inline-block;*/
          font-size: 14px;
        }
      }

    }



</style>
