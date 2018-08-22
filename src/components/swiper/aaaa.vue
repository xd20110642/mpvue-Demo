<template>
  <div class="aaaa">
    <swiper indicator-dots="true" :autoplay="autoplay"
            :interval="interval" :duration="duration" :circular="circular" >
      <block v-for="(item,index) of imgUrls" :key="index">
        <swiper-item>
          <img :src="item" class="slide-image" />
        </swiper-item>
      </block>
    </swiper>
  </div>

</template>

<script>
  export default {
    name: "aaaa",
    data(){
      return{
        imgUrls: [
          '../../assets/images/banner-01.png',
          '../../assets/images/banner-01.png',
          '../../assets/images/banner-01.png',
        ],
        autoplay:true,
        interval:5000,
        duration:1000,
        circular:true
      }
    }
  }
</script>

<style scoped lang="scss">
@import "../../commos/commos.scss";
    swiper{
      height: rpx(392);
    }
    img{
      width: 100%;
     height: rpx(392);
    }

</style>
