<template>
  <div>
    <head />
    <div class="wrapper">
      <img class="dp" src="~/assets/dp.jpg">
      <div class="greeting">
        Hi! I'm
      </div>
      <div class="parvez-mia">
        Parvez Mia
      </div>
      <div class="pz1971">
        (pz1971)
      </div>
    </div>
    <div class="bio">
      <div class="bio-item">
        Competitive Programmer
      </div><div class="separator" />
      <div class="bio-item">
        Undergrad Student
      </div><div class="separator" />
      <div class="bio-item">
        Software Developer
      </div>
    </div>
    <contact-me />
    <horizontal-line />
    <div class="button-group">
      <nuxt-link class="about-button" to="/about">
        <btn-1 text="About Me" />
      </nuxt-link>
      <nuxt-link class="about-button" to="/portfolio">
        <btn-1 text="My Works" />
      </nuxt-link>
      <nuxt-link class="about-button" to="/blog">
        <btn-1 text="Blog" />
      </nuxt-link>
    </div>
  </div>
</template>

<script>
import Btn1 from '~/components/btn-1.vue'
import contactMe from '~/components/contact-me.vue'
import HorizontalLine from '~/components/horizontal-line.vue'
export default {
  components: { contactMe, HorizontalLine, Btn1 },
  head: {
    title: 'pz1971 Blog - home',
    meta: [
      {
        hid: 'pz1971 hompage, bio, about, blog, parvez mia',
        name: 'pz1971 blog',
        content: 'Hi! I\'m Parvez Mia (pz1971). I\'m a Competitive Programmer, currently doing undergraduage (B.Sc.) in CSE and I\'m working to be a software developer.'
      },
      {
        name: 'google-site-verification',
        content: 'SUWESRJ1uPLBQuF_S3xiRkjWx9KLqPG8zRTJiI6YgLs'
      }
    ]
  }
}
</script>

<style>
@import '~/assets/styles/variables.css';

.wrapper {
  margin: auto;
  width: 50%;
  padding: 10px;
  text-align: center;
}

.dp {
  border-radius: 50%;
  max-width: 13rem;
  margin-bottom: 2%;
}

.greeting {
  font-size: var(--medium-font-size);
  font-family: monospace;
}
.parvez-mia {
  font-weight: bold;
  font-size: var(--large-font-size);
  font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
}
.pz1971 {
  font-size: var(--medium-font-size);
  font-family: monospace;
}
.pz1971:hover {
  transform: rotate(10deg);
}

.bio {
  margin: auto;
  text-align: center;
  padding: 1ch;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.separator {
  width: 0.3rem;
  background-color: black;
  margin-left:  1ch;
  margin-right: 1ch;
}
.bio-item {
  font-size: var(--small-font-size);
}
.bio-item:hover {
  transform: scale(1.05, 1.05);
  color: red;
}

.button-group {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 1ch;
}
</style>
