<template>
  <div>
    <v-container>
      <v-card class="mx-auto" height="600" width="350">
        <v-cad-title class="d-flex justify-center">計算機</v-cad-title>
        <v-row class="mx-2">
          <v-col>
            <v-text-field class="pb-0" solo disabled></v-text-field>
          </v-col>
        </v-row>
        <v-row class="mx-2">
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="cal" block color="primary">AC</v-btn>
          </v-col>
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="cal" block color="primary">+/-</v-btn>
          </v-col>
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="cal" block color="primary">%</v-btn>
          </v-col>
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="cal" block color="primary">/</v-btn>
          </v-col>
        </v-row>

        <v-row class="mx-2">
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="number" block color="primary">7</v-btn>
          </v-col>
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="number" block color="primary">8</v-btn>
          </v-col>
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="number" block color="primary">9</v-btn>
          </v-col>
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="cal" block color="primary">X</v-btn>
          </v-col>
        </v-row>

        <v-row class="mx-2">
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="number" block color="primary">4</v-btn>
          </v-col>
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="number" block color="primary">5</v-btn>
          </v-col>
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="number" block color="primary">6</v-btn>
          </v-col>
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="cal" block color="primary">-</v-btn>
          </v-col>
        </v-row>

        <v-row class="mx-2">
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="number" block color="primary">3</v-btn>
          </v-col>
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="number" block color="primary">2</v-btn>
          </v-col>
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="number" block color="primary">1</v-btn>
          </v-col>
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="cal" block color="primary">+</v-btn>
          </v-col>
        </v-row>

        <v-row class="mx-2">
          <v-col class="px-1" cols="12" sm="6">
            <v-btn class="number" block color="primary">0</v-btn>
          </v-col>
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="number" block color="primary">.</v-btn>
          </v-col>
          <v-col class="px-1" cols="12" sm="3">
            <v-btn class="cal" block color="primary">=</v-btn>
          </v-col>
        </v-row>
      </v-card>
    </v-container>
  </div>
</template>

<script>
export default {
  layout: 'custom',
  data() {
    return {
      data: 0,
      result: 0
    }
  },
  mounted() {
    // 宣告變數
    const number = document.getElementsByClassName('number')
    const calFunction = document.getElementsByClassName('cal')
    // const count = 0

    let i = 0
    for (i = 0; i < number.length; i++) {
      number[i].addEventListener('click', function() {
        // 如果 number class 被點擊後，執行的 function
      })
    }

    calFunction[0].addEventListener('click', function() {
      // 如果 cal class 被點擊後，執行的 function
    })
  }
}
</script>

<style lang="scss" scoped></style>
