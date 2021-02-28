<template>
  <div>
    <div>記事詳細ページ</div>
    <div>
      <!-- nuxt-link は必要箇所のみ読み込み = 早い -->
      <nuxt-link to="/articles/10/edit">Nuxt Link</nuxt-link>
    </div>
    <div>
      <!-- a タグはページ全体を読み込む = nuxt-link に比べ遅い -->
      <a href="/articles/10/edit">a タグ</a>
    </div>
    <div>
      <nuxt-link to="/articles/10/update"> 更新ページ </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    const foo = 'foo'
    console.log(foo)
  },
}
</script>
