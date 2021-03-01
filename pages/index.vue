<template>
  <div>
    <!-- {{}} で囲むと javascript が書ける（マスタッシュ記法） -->
    <div class="number">{{ count }}</div>
    <!-- v-記法をディレクティブと呼ぶ
    @ で省略できる
    @click = v-on:click  -->
    <!-- <button @click="plus" class="button">+</button>
    <button @click="minus" class="button">-</button> -->

    <!-- Vuetify で簡単にボタン作成 -->
    <!-- <v-btn class="mx-1" fab dark color="blue" @click="plus">
      <v-icon dark> mdi-plus </v-icon>
    </v-btn>

    <v-btn class="mx-1" fab dark color="orange" @click="minus">
      <v-icon dark> mdi-minus </v-icon>
    </v-btn> -->

    <!-- <counter-button /> で 閉じタグと同じ表現 -->
    <!-- props で設定した値を指定する -->
    <counter-button kind="plus" color="blue" />
    <counter-button kind="minus" color="orange" />
  </div>
</template>

<script>
// ①作成したコンポーネントの読み込み
import CounterButton from '@/components/CounterButton.vue'

export default {
  // ②プロパティに指定
  components: {
    CounterButton,
  },
  // data というメソッドを作成
  data() {
    // return でオブジェクトのプロパティが count: 0 のものを返している
    // {} で囲んだものはオブジェクトになる（復習）
    return {
      count: 100,
    }
  },
  // () の中に : として定義するから
  // methods は export default のプロパティ
  methods: {
    plus() {
      this.count += 1
    },
    minus() {
      this.count -= 1
    },
  },
}
</script>

<style lang="scss">
.number {
  font-size: 64px;
}

// .button {
//   font-size: 32px;
//   border: 2px solid white;
//   border-radius: 4px;
//   width: 48px;
//   height: 48px;
// }
</style>
