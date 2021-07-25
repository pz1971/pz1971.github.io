<template>
  <div>
    <nav-bar location="#" />
    <article>
      <nuxt-content :document="article" />
    </article>
  </div>
</template>

<script>
import navBar from '~/components/nav-bar.vue'
export default {
  components: { navBar },
  async asyncData ({ $content, params }) {
    const article = await $content('blog', params.slug).fetch()
    return { article }
  }
}
</script>

<style>

</style>
