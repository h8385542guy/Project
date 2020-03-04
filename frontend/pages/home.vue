<template>
  <div>
    <h1 id="home">這是首頁@@@@</h1>
    <div>
      <p>我們可以在這邊寫一點東西...</p>
    </div>

    <img :src="require('~/static/AAIeXUw.jpg')" />

    <!-- 使用 computed 做操作 -->
    <div>
      <input v-model="message" type="text" placeholder="請輸入資料" />
      <p>反轉訊息：{{ reversedMessage }}</p>
    </div>

    <!-- 使用 methods 做操作 -->
    <v-btn @click="clickMe()">按我</v-btn>
  </div>
</template>

<script>
export default {
  // 指定使用的 layout，如果不指定的話預設是 default
  layout: 'custom',
  components: {},
  asyncData() {
    // 放在 component 不能操作
    return { message: '789' }
  },
  data() {
    return {
      // 設定變數
      message: '123'
    }
  },
  computed: {
    // 主動式的 function
    reversedMessage() {
      return this.message
        .split('')
        .reverse()
        .join('')
    }
  },
  mounted() {
    // 載入資料
    this.message = '456'
  },
  beforeCreate() {
    // 這是 beforeCreate
  },
  methods: {
    // 被動式的 function，例如:click 之後作用
    clickMe() {
      alert('你按了我!!')
    }
  }
}
</script>

<style lang="scss" scoped>
// 這邊可以寫 CSS 的東西
#home {
  color: blue;
}
</style>
