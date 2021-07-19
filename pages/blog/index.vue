<template>
  <div>
    <nav-bar location="blog" class="the-nav-bar" />
    <div class="articles">
      <div v-for="article of articles" :key="article" class="article">
        <nuxt-link :to="{ name: 'blog-slug', params: { slug:article.slug } }">
          <img v-if="article.thumbnail!='null.jpg'" :src="require(`~/assets/resources/${article.thumbnail}`)" alt="">
          <div class="detail">
            <h3>{{ article.title }}</h3>
            <p>{{ article.description }}</p>
          </div>
        </nuxt-link>
        <hr>
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

<style scoped>
.the-nav-bar{
  margin-left: 10%;
  margin-right: 10%;
}
.articles{
  margin-left: 10%;
  margin-right: 10%;
}
.article{
  margin-top: 3ch;
}
hr {
  margin-top: 3ch;
}
@media only screen and (max-width: 500px){
  .the-nav-bar{
    margin-left: 0%;
    margin-right: 0%;
  }
  .articles{
    margin-left: 5%;
    margin-right: 5%;
  }
}
</style>
