<template>
  <v-app>
    <v-container>
      <app-bar></app-bar>
      <nuxt />
    </v-container>
  </v-app>
</template>

<script>
export default {
  components: {
    // import component
    AppBar: () => import('~/components/base/AppBar.vue')
  }
}
</script>

<style lang="scss" scoped>
#app {
  background-color: white;
}
</style>
