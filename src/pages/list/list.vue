<template>
    <div class="list">
      <foodlist
        :title="name"
      ></foodlist>
      <foodlist
        :title="name"
      ></foodlist>
      <foodlist
        :title="name"
      ></foodlist>
      <foodlist
        :title="name"
      ></foodlist>
    </div>
</template>

<script>
  import foodlist from '../../components/foodlist/foodlist.vue'
    export default {
        name: "list",
        data(){
          return{
          name:'韩国烤肉'
          }
        },
        components:{
          foodlist
        }
    }
</script>

<style scoped lang="scss">

</style>
