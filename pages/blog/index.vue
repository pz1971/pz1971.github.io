<template>
  <div>
    <div class="articles">
      <div v-for="article of articles" :key="article" class="article">
        <nuxt-link :to="{ name: 'blog-slug', params: { slug:article.slug } }">
          <img :src="require(`~/assets/resources/${article.thumbnail}`)" alt="">
          <div class="detail">
            <h3>{{ article.title }}</h3>
            <p>{{ article.description }}</p>
          </div>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const articles = await $content('blog', params.slug)
      .only(['title', 'description', 'thumbnail', 'slug'])
      .sortBy('createdAt', 'desc')
      .fetch()
    return { articles }
  }
}
</script>

<style>

</style>
