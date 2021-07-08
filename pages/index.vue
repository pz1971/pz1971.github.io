<template>
  <div>
    <head />
    <!-- class names defines their identity -->
    <div class="wrapper">
      <img class="dp" src="~/assets/dp.jpg">
      <div class="greeting">
        Hi! I'm
      </div>
      <div class="name">
        Parvez Mia
      </div>
      <div class="handle">
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
    <div class="contact-me-wrapper">
      <!-- contact-me properties are in components folder -->
      <contact-me />
    </div>
    <hr class="hr1">
    <div class="button-group">
      <nuxt-link class="nav-buttons" to="/about">
        <btn-1 text="About Me" />
      </nuxt-link>
      <nuxt-link class="nav-buttons" to="/portfolio">
        <btn-1 text="My Works" />
      </nuxt-link>
      <nuxt-link class="nav-buttons" to="/blog">
        <btn-1 text="Blog" />
      </nuxt-link>
    </div>
  </div>
</template>

<script>
import Btn1 from '~/components/btn-1.vue'
import contactMe from '~/components/contact-me.vue'
export default {
  components: { contactMe, Btn1 },
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
  padding-top: 10px;
  padding-bottom: 10px;
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
.name {
  font-weight: bold;
  font-size: var(--large-font-size);
  font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
}
.handle {
  font-size: var(--medium-font-size);
  font-family: monospace;
}
.handle:hover {
  transform: rotate(10deg);
}
.contact-me-wrapper {
  display: flex;
  justify-content: center;
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
.hr1 {
  margin-left: 20%;
  margin-right: 20%;
}
.button-group {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.nav-buttons {
  margin: 1ch;
}

@media only screen and (max-width: 500px) {
  :root{
    --small-font-size: 1rem ;
    --medium-font-size: 1.25rem ;
    --large-font-size: 1.5rem ;
  }
  .dp {
    max-width: 10rem;
  }
  .button-group {
    display:flexbox;
    flex-direction: column;
    flex-wrap: nowrap;
    margin-top: 2ch;
    width: 100%;
    padding-left: 10%;
    padding-right: 10%;
  }
  .nav-buttons {
    margin: auto;
    width: inherit;
    margin-top: 0.5ch;
  }
}
</style>
