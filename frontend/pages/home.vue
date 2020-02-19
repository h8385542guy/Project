<template>
  <div>
    <h1 id="home">這是首頁@@@@</h1>
    <div>
      <p>我們可以在這邊寫一點東西...</p>
    </div>
    <div v-for="i in 5" :key="i">
      <cards></cards>
    </div>
  </div>
</template>

<script>
export default {
  // 指定使用的 layout，如果不指定的話預設是 default
  layout: 'custom',
  components: {
    Cards: () => import('~/components/base/Card')
  },
  data() {
    return {
      imageTitle1: '這是圖片一的標題'
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
