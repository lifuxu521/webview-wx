<template>
  <div class="box">
    <br><br>
    <Button type="success" long shape="circle" @click="setCookie()">登录存储cookie</Button>
    <br><br>
  </div>
</template>
<script>
export default {
  data () {
    return {

    }
  },
  mounted: function () {
  },
  methods: {
    setCookie () {
      document.cookie = 'test=' + 'hello'
      this.$Message.success('存储成功')
    }
  }
}
</script>
<style scoped>
</style>
