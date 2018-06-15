<template>
  <div class="container">
    <raceList></raceList>
  </div>
</template>

<script>
import card from '@/components/card'
import raceList from '@/components/race-list'

export default {
  components: {
    raceList
  },
  data () {
    return {
      motto: 'Hello World',
      userInfo: {}
    }
  },

  components: {
    card
  },

  methods: {
    bindViewTap () {
      const url = '../logs/main'
      wx.navigateTo({ url })
    },
    getUserInfo () {
      // 调用登录接口
      wx.login({
        success: () => {
          wx.getUserInfo({
            success: (res) => {
              this.userInfo = res.userInfo
            }
          })
        }
      })
    },
    clickHandle (msg, ev) {
      console.log('clickHandle:', msg, ev)
    }
  },

  created () {
    // 调用应用实例的方法获取全局数据
    this.getUserInfo()
  }
}
</script>

<style scoped>
  .background {
    position: fixed;
    z-index: -1;
    width: 100vw;
    height: 100vh;
    top: 0;
  }
</style>
