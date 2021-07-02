<template>
  <div class="container">
    <nuxt-link v-if="location!='home'" to="/">
      <btn-2 text="Home" />
    </nuxt-link>
    <nuxt-link v-if="location!='about'" to="/about">
      <btn-2 text="About Me" />
    </nuxt-link>
    <nuxt-link v-if="location!='portfolio'" to="/portfolio">
      <btn-2 text="My Works" />
    </nuxt-link>
    <nuxt-link v-if="location!='blog'" to="/blog">
      <btn-2 text="Blog" />
    </nuxt-link>
  </div>
</template>

<script>
export default {
  props: {
    location: {
      type: String,
      required: true
    }
  }
}
</script>

<style>
.container {
  display: flex;
}
</style>
