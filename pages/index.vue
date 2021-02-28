<template>
  <div>
    <!-- {{}} で囲むと javascript が書ける（マスタッシュ記法） -->
    <div>{{ count }}</div>
    <!-- v-記法をディレクティブと呼ぶ
    @ で省略できる
    @click = v-on:click  -->
    <button @click="plus">+</button>
    <button @click="minus">-</button>
  </div>
</template>

<script>
export default {
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
