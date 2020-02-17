<template>
  <div>
    <h1 id="home">這是首頁@@@@</h1>
    <div>
      <p>我們可以在這邊寫一點東西...</p>
    </div>

    <!-- 製作卡片 (card) -->
    <v-card width="400px">
      <v-img
        class="white--text align-end"
        height="200px"
        src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
      >
        <!-- 用變數代替字串 {{ 變數名稱 }} -->
        <v-card-title>{{ imageTitle1 }}</v-card-title>
      </v-img>
    </v-card>

    <v-card class="pt-2" width="400px">
      <v-img
        class="white--text align-end"
        height="200px"
        src="https://cdn.vuetifyjs.com/images/cards/house.jpg"
      >
      </v-img>
      <v-card-title class="pb-0">這是卡片2的標題</v-card-title>

      <v-card-text class="text--primary">
        <div>
          這是第二章卡片的內容，這是第二章卡片的內容，這是第二章卡片的內容。
        </div>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  // 指定使用的 layout，如果不指定的話預設是 default
  layout: 'custom',
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
