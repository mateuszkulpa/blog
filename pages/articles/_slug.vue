<template>
  <article>
    <nuxt-link to="/">Home page</nuxt-link>
    <h1>{{ page.title }}</h1>
    <nuxt-content :document="page" />
  </article>
</template>

<script>
export default {
  async asyncData({ $content, params: { slug } }) {
    const page = await $content(`articles/${slug}`).fetch()

    return {
      page
    }
  }
}
</script>

<style lang="scss" scoped>
article {
  margin: 4rem auto;
  max-width: 700px;
}
</style>
