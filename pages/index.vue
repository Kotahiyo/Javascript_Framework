<template>
  <div>
    <!-- {{}} で囲むと javascript が書ける（マスタッシュ記法） -->
    <div>{{ count }}</div>
  </div>
</template>

<script>
export default {
  // data というメソッドを作成
  data() {
    // return でオブジェクトのプロパティが count: 0 のものを返している
    // {} で囲んだものはオブジェクトになる（復習）
    return {
      count: 0,
    }
  },
}
</script>
