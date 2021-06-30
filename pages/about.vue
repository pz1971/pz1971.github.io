<template>
  <div class="container">
    <div class="wrapper1">
      <img class="dp" src="~/assets/dp.jpg">
      <div class="wrapper2">
        <div class="name">
          Parvez Mia
        </div>
        <div class="handle">
          (pz1971)
        </div>
        <contact-me />
      </div>
    </div>
  </div>
</template>

<script>
import contactMe from '~/components/contact-me.vue'
export default {
  components: { contactMe }
}
</script>

<style>
@import '~/assets/styles/variables.css';
.container {
  display: flex;
  justify-content: center;
}
.dp {
  border-radius: 50%;
  max-width: 12rem;
  margin-right: 2%;
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
.wrapper1 {
  display: flex;
  align-items: center;
  width: 500px;
}
.wrapper2 {
  display: flex;
  flex-direction: column;
  align-items: center;
}

</style>
