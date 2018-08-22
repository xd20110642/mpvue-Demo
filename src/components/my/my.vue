<template>
    <div class="my">
      <div class="my-top">
        <div class="my-top-img">
          <img src="../../assets/images/avatar.png" alt="">
        </div>

      </div>
    </div>
</template>

<script>
    export default {
        name: "my"
    }
</script>

<style scoped lang="scss">
  @import "../../commos/commos.scss";
    .my{
      width: 100%;
      .my-top{
        width: 100%;
        height: rpx(407);
        background-color: #ed702d;
        /*垂直居中*/
        display: flex;
        justify-content: center;
        align-items: center;
          .my-top-img{
          width: rpx(219);
          height: rpx(219);
          border: rpx(5) solid black;
          border-radius: 50%;
          img{
            width: rpx(219);
            height: rpx(219);
          }
        }

      }
    }
</style>
