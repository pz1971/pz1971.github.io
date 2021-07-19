<template>
  <div>
    <nav-bar location="#" class="the-nav-bar" />
    <Nuxt class="blog-body-container" />
    <div class="footer" />
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.the-nav-bar {
  margin-left: 10%;
  margin-right: 10%;
}
.blog-body-container {
  margin-left: 10%;
  margin-right: 10%;
}
.footer{
  height: 5rem;
}

@media only screen and (max-width: 500px){
  .the-nav-bar{
    margin-left: 0%;
    margin-right: 0%;
  }
  .blog-body-container{
    margin-left: 5%;
    margin-right: 5%;
  }
}
</style>
