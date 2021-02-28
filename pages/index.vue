<template>
  <div>
    <!-- {{}} で囲むと javascript が書ける（マスタッシュ記法） -->
    <div class="number">{{ count }}</div>
    <!-- v-記法をディレクティブと呼ぶ
    @ で省略できる
    @click = v-on:click  -->
    <button @click="plus" class="button">+</button>
    <button @click="minus" class="button">-</button>
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

<style lang="scss">
.number {
  font-size: 64px;
}

.button {
  font-size: 32px;
  border: 2px solid white;
  border-radius: 4px;
  width: 48px;
  height: 48px;
}
</style>
