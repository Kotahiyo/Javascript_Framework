<template>
  <div>
    <!-- v-ifと仲間たち -->
    <div v-if="score >= 80">おめでとう！</div>
    <div v-else-if="score >= 30">もっといける！</div>
    <div v-else>頑張ろう！</div>

    <a :href="googleLink">Googleへのリンク</a>
    <!-- v-show は false の場合、非表示になる -->
    <!-- <div v-show="isShown">見えるかな？</div>
    <v-btn @click="toggleShown">ボタン押すと消える</v-btn> -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      isShown: true,
      score: 80,
      googleLink: 'https://www.google.com/?hl=ja',
    }
  },
  methods: {
    toggleShown() {
      // ! で反転する
      this.isShown = !this.isShown
    },
  },
}
</script>
