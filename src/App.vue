<script>
export default {
  //相当于原生的app.js
  created () {
    // 调用API从本地缓存中获取数据
    const logs = wx.getStorageSync('logs') || []
    logs.unshift(Date.now())
    wx.setStorageSync('logs', logs);//存入本地缓存
    console.log('1')
  },
  onLaunch(options){ //小程序初始化
    console.log(options)
    console.log('2');
  },
  onShow(options){//显示前台
    console.log("我是onShow3");
    let scene=options.scene
    if (scene===1011){
      console.log('我是通过扫描二维码进来的')
    }
    console.log(options)
  },
  onHide() {
  console.log("我退出了")
  },
}
</script>

<style>
  /* 这部分相当于原生小程序的 app.wxss */
.container {
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  padding: 200rpx 0;
  box-sizing: border-box;
}
/* this rule will be remove */
* {
  transition: width 2s;
  -moz-transition: width 2s;
  -webkit-transition: width 2s;
  -o-transition: width 2s;
}
</style>
