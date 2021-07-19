<template>
  <div>
    <nav-bar location="blog" class="the-nav-bar" />
    <div class="articles">
      <div v-for="article of articles" :key="article" class="article">
        <nuxt-link :to="{ name: 'blog-slug', params: { slug:article.slug } }" class="link-to-article">
          <img v-if="article.img!='null.jpg'" :src="require(`~/assets/resources/${article.img}`)" :alt="article.alt" class="the-thumbnail-img">
          <div class="detail">
            <h3>{{ article.title }}</h3>
            <p>{{ article.description }}</p>
          </div>
        </nuxt-link>
        <h5 class="article-creation-date">
          {{ formatDate(article.createdAt) }}
        </h5>
        <hr>
      </div>
    </div>
    <div class="the-footer" />
  </div>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const articles = await $content('blog', params.slug)
      .only(['title', 'description', 'img', 'alt', 'slug', 'createdAt'])
      .sortBy('createdAt', 'desc')
      .fetch()
    return { articles }
  },
  methods: {
    formatDate (date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('en', options)
    }
  }
}
</script>

<style scoped>
.the-nav-bar{
  margin-left: 15%;
  margin-right: 15%;
}
.articles{
  margin-left: 15%;
  margin-right: 15%;
}
.article{
  margin-top: 3ch;
  float: left;
}
.link-to-article{
  display: flex;
}
.the-thumbnail-img{
  max-height: 10rem;
}
.article-creation-date{
  margin-top: 2ch;
}
hr {
  margin-top: 3ch;
}
.the-footer{
  height: 5rem;
}

a{
  text-decoration: none;
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
