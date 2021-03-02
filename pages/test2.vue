<template>
  <div>
    <div>ライフサイクルテスト</div>
    <v-text-field v-model="number" />
    <div>数値: {{ number }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: 0,
    }
  },
  created() {
    console.log('created')
  },
  mounted() {
    console.log('mounted')
  },
  updated() {
    console.log('updated')
  },
}
</script>

<style lang="scss"></style>
