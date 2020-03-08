<template>
  <div>
    <!-- 參考 vuetify: https://vuetifyjs.com/en/components/app-bars -->
    <v-app-bar color="green accent-4" dense dark>
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

      <v-toolbar-title>這是 AppBar</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon class="d-none">
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon class="d-none">
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-menu left bottom>
        <template v-slot:activator="{ on }">
          <v-btn icon class="d-none" v-on="on">
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item v-for="n in 5" :key="n" @click="() => {}">
            <v-list-item-title>Option {{ n }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>

    <!-- 左側選單 -->
    <v-navigation-drawer v-model="drawer" absolute left temporary>
      <v-list nav dense class="ml-2">
        <!-- 側欄選單項目 -->
        <v-list-item :to="'/home'">
          <v-list-item-title>首頁</v-list-item-title>
        </v-list-item>
        <v-list-item :to="'/users'">
          <v-list-item-title>會員資料</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      drawer: false
    }
  }
}
</script>

<style lang="scss" scoped></style>
