<template>
  <ul class="container">
    <li v-if="location!='home'" class="list-item">
      <nuxt-link to="/" class="a-link">
        <img class="icon" src="~/assets/dp.jpg" alt=""> Home
      </nuxt-link>
    </li>
    <li v-if="location!='about'" class="list-item">
      <nuxt-link to="/about" class="a-link">
        About Me
      </nuxt-link>
    </li>
    <li v-if="location!='portfolio'" class="list-item">
      <nuxt-link to="/portfolio" class="a-link">
        My Works
      </nuxt-link>
    </li>
    <li v-if="location!='blog'" class="list-item">
      <nuxt-link to="/blog" class="a-link">
        Blog
      </nuxt-link>
    </li>
  </ul>
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

<style scoped>
.container {
  display: flex;
  list-style-type: none;
  padding: 0;
  overflow: hidden;
  background-color: rgb(61, 61, 61);
}

.icon {
  max-height: 1.1rem;
  border-radius: 50%;
  margin-right: 1ch;
}

.list-item {
  float: left;
  width: 33.33%;
}

.a-link {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

.a-link:hover {
  background-color: rgb(0, 0, 0);
}
</style>
