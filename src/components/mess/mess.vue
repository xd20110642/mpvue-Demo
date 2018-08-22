<template>
    <div class="mess">
        <div class="mess-top">
          <div class="title">
           {{title}}
          </div>
          <div class="time">
            2017-12-05
          </div>
        </div>
        <div class="mess-content">
          <img src="http://placehold.it/700x300" alt="">
          <div class="mess-text">
            <p>越奴力，越幸福</p>
          </div>
        </div>
      <div class="mess-footer">
        <navigator url="/page/index/index?title=1">
          查看详情
        </navigator>
      </div>
    </div>
</template>

<script>
    export default {
        name: "mess",
      props:{
          title:{
            type:String,
            default:'我是一个标题'
          }
      }
    }
</script>

<style scoped lang="scss">
  @import "../../commos/commos.scss";
    .mess{
      width: 90%;
      border: 1px solid #ccc;
      background-color: #fff;
      margin: 10px auto;
      box-shadow: 0 0 10px #ccc;
      border-radius: 10px;
      overflow: hidden;
      .mess-top{
        width: 100%;
        @include border-1px-bottom(#ccc);
        .title{
          text-align: center;
          font-size: 14px;
          line-height:24px;
          font-weight: 700;
        }
        .time{
          text-align: center;
          font-size: 12px;
          color: #ccc;
        }
      }
      .mess-content{
        text-align: center;
        margin-top: 10px;
        img{
          height: rpx(300);
        }
        .mess-text{
          float: left;
          padding-left: 12px;
          font-size: 12px;
          color: #cccc;
        }
      }
      .mess-footer{
        float: left;
        margin-top: 10px;
        width: 100%;
        font-size: 14px;

      }
    }
</style>
