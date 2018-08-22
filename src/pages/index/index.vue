<template>
      <div class="content">
        <button @click="a" v-show="!show">点击开始显示</button>
       <div v-show="show">
        <div class="slider1">
          <aaaa></aaaa>
        </div>
        <div class="meun">
          <meun></meun>
        </div>
        <!--分割组件-->
        <ceng></ceng>
        <div class="enter">
          <div class="enter-item">
            <enter
              :type1="1"
            ></enter>
          </div>
          <div class="enter-item">
            <enter></enter>
          </div>
        </div>
        <!--<button open-type="share"></button>-->
       </div>
      </div>
</template>

<script>
  import aaaa from '../../components/swiper/aaaa.vue'
  import meun from  '../../components/meun/meun.vue'
  import enter from '../../components/enter/enter.vue'
  import ceng from '../../components/ceng/ceng.vue'
    export default {
        data(){
          return{
            show:false
          }
        },
      components:{
        aaaa,
        meun,
        enter,
        ceng
      },
      onShareAppMessage(res){
        return {
          title: '自定义转发标题',
          path: '/page/user?id=123'
        }
      },
      methods:{
          a(){
            this.show=!this.show
          }
      }
    }
</script>

<style scoped lang="scss">
  @import "../../commos/commos.scss";

  .content{
   overflow: hidden;
    .slider1{
      width: 100%;
      text-align: center;
    }
    .meun{
    margin-top: rpx(20);
    }
    .enter{
      display: flex;
      width: 100%;
      height: rpx(172);
      justify-content: center;
      padding: rpx(20) rpx(10);
      .enter-item{
       width: 50%;
      }
    }
    button{
      width: 100%;
      /*height:;*/
    }
  }


</style>
