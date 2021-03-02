<template>
  <div>
    <!-- v-ifと仲間たち -->
    <div v-if="score >= 80">おめでとう！</div>
    <div v-else-if="score >= 30">もっといける！</div>
    <div v-else>頑張ろう！</div>

    <!-- v-bind -->
    <!-- <a :href="googleLink">Googleへのリンク</a> -->
    <img :src="imageUrl()" width="100px" />
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
      score: 0,
      googleLink: 'https://www.google.com/?hl=ja',
    }
  },
  methods: {
    toggleShown() {
      // ! で反転する
      this.isShown = !this.isShown
    },
    imageUrl() {
      if (this.score >= 80) {
        return 'https://2.bp.blogspot.com/-zDsrPiqkR_0/U0pTNj7lpoI/AAAAAAAAfGA/2Z1onz10tAw/s800/grade2_yokudekimashita.png'
      } else if (this.score >= 30) {
        return 'https://2.bp.blogspot.com/-wJDmO2MIKkg/U0pTOEZT-JI/AAAAAAAAfGc/p9uwt9Msq9A/s800/grade3_ganbarimashita.png'
      } else {
        return 'https://2.bp.blogspot.com/-Bc8NTQ2PqY8/U0pTOuIDWQI/AAAAAAAAfGY/1RU2LKdozKs/s800/grade5_ganbarimasyou.png'
      }
    },
  },
}
</script>
