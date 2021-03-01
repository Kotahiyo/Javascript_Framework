<template>
  <!-- v-bind で値を紐付け。: で省略。指定しているのは設定したプロパティ -->
  <!-- methods 内で作成したメソッドを @click で指定 -->
  <v-btn class="mx-1" fab dark :color="color" @click="click">
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
  methods: {
    // click メソッドを作成
    click() {
      // 渡す値の名前を指定
      this.$emit('click')
    },
  },
}
</script>
