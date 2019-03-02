<template>
  <div class="box">
     <br><br>
     <br><br>
     <br><br>
     <Button type="success" long shape="circle" @click="toLogin()">去登录</Button>
     <Button type="error" long shape="circle" @click="getCookie()">查看cookie</Button>
     <br><br>
     <br><br>
     <br><br>
  </div>
</template>
<script>
import cookie from '@/lib/cookie'
export default {
  data () {
    return {

    }
  },
  mounted: function () {
  },
  methods: {
    getCookie () {
      const test = cookie.get('test') + ''
      this.$Message.info(test)
    },
    toLogin () {
      wx.miniProgram.navigateTo({url: '/loginWebview/index'})
    }
  }
}
</script>
<style scoped>
</style>
