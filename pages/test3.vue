<template>
  <div>
    <div>ライフサイクルテスト</div>
    <v-text-field ref="number" v-model="number" />
    <div>数値: {{ number }}</div>

    <div :class="$style.container" v-for="user in users" :key="user.id">
      <div>名前: {{ user.name }}</div>
      <div>電話番号: {{ user.phone }}</div>
      <div>メールアドレス: {{ user.email }}</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: 0,
      users: [],
    }
  },
  // async created() {
  //   try {
  //     const response = await this.$axios.get(
  //       'http://jsonplaceholder.typicode.com/userssss'
  //     )
  //     console.log(response)
  //   } catch (err) {
  //     const res = err.response
  //     console.log(res)
  //   }
  // },
  created() {
    new Promise((resolve, reject) => {
      this.$axios
        .get('https://jsonplaceholder.typicode.com/users')
        .then((response) => {
          resolve(response.data)
        })
        .catch((err) => {
          reject(err.response)
        })
    })
      .then((data) => {
        console.log(data)
        this.user = data
      })
      .catch((response) => {
        console.log(response)
      })
  },
  mounted() {
    console.log('mounted')
    this.$refs.number.focus()
  },
  updated() {
    console.log('updated')
    console.log(this.number)
  },
}
</script>

<style lang="scss" module>
.container {
  margin: 10px 0;
  padding: 8px;
  border: 2px solid #ccc;
  border-radius: 2px;
}
</style>
