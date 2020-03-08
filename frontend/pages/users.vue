<template>
  <div>
    <v-container>
      <div class="title ma-2">從 API 取得 User 資料</div>

      <!-- 將 api 拿到的 user 資料變成表格形式 -->
      <v-simple-table>
        <template v-slot:default>
          <thead>
            <tr>
              <th class="text-left">姓名</th>
              <th class="text-left">用戶名</th>
              <th class="text-left">信箱</th>
              <th class="text-left">電話</th>
              <th class="text-left">網站</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="user in users" :key="user.id">
              <td>{{ user.name }}</td>
              <td>{{ user.username }}</td>
              <td>{{ user.email }}</td>
              <td>{{ user.phone }}</td>
              <td>{{ user.website }}</td>
            </tr>
          </tbody>
        </template>
      </v-simple-table>
    </v-container>
  </div>
</template>

<script>
export default {
  layout: 'custom',
  data() {
    return {
      users: null
    }
  },
  mounted() {
    this.getUsers()
  },
  methods: {
    // 取得 sample user 的 api 資料
    // 參考網站: https://jsonplaceholder.typicode.com/
    getUsers() {
      this.$axios
        .get('https://jsonplaceholder.typicode.com/users')
        .then((res) => {
          this.users = res.data
        })
    }
  }
}
</script>

<style lang="scss" scoped></style>
