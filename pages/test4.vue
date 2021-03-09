<template>
  <v-btn @click="toggleSidebar()">サイドバー</v-btn>
</template>

<script>
export default {
  methods: {
    toggleSidebar() {
      this.$store.dispatch('layout/toggleSidebar')
    },
  },
}
</script>
