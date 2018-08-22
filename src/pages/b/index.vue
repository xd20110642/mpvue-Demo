<template>
  <div class="b">
      <mess
      :title="123"
      ></mess>
      <mess
        :title="456"
      ></mess>
      <mess :title="789"></mess>
  </div>
</template>

<script>
  import mess from '../../components/mess/mess.vue'
    export default {
        name: "index",
        components:{
          mess
        }

    }
</script>

<style scoped lang="scss">
  .b{
    width: 100%;
    background-color: #eee;
  }
</style>
