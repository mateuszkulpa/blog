<template>
  <div class="container">
    <h1>Blog</h1>
    <div>
      <h3>posts</h3>
      <ul>
        <li v-for="article in articles" :key="article.slug">
          <nuxt-link :to="`/article/${article.slug}`">
            {{ article.title }}
          </nuxt-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const articles = await $content('articles').fetch()
    // eslint-disable-next-line no-console
    console.log(articles)
    return { articles }
  }
}
</script>

<style></style>
