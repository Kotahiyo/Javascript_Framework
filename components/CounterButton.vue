<template>
  <!-- v-bind で値を紐付け。: で省略。指定しているのは設定したプロパティ -->
  <v-btn class="mx-1" fab dark :color="color" @click="plus">
    <!-- マスタッシュ記法で変更したい部分を切り取ってプロパティを指定 -->
    <v-icon dark> mdi-{{ kind }} </v-icon>
  </v-btn>
</template>

<script>
export default {
  props: {
    // kind と color のプロパティを渡してデフォルト値を設定
    kind: {
      type: String,
      default: 'plus',
    },
    color: {
      type: String,
      default: 'blue',
    },
  },
}
</script>
