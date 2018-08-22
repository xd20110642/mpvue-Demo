<template>
    <div class="enter">
      <navigator >
        <img :src="url" alt="" >
        <!--<img src="../../assets/images/link-02.png" alt="">-->
      </navigator>
    </div>
</template>

<script>
    export default {
        name: "enter",
      props:{
          type1:{
            type:Number,
            default:2
          }
      },
      data(){
          return{

          }
      },
      computed:{
          url(){
            return `../../assets/images/link-0${this.type1}.png`;
        }
      },
      create(){
          console.log(url)
      }
    }
</script>

<style scoped lang="scss">
  @import "../../commos/commos.scss";
  .enter{
    width: 100%;
    margin: 0 auto;
    text-align: center;
    img{
      width: rpx(320);
      height:rpx(172)
    }
  }
</style>
