<template>
  <div>
    <img class="dp" src="~/assets/dp.jpg">
    <div class="parvez-mia">
      Parvez Mia
    </div>
    <div class="pz1971">
      (pz1971)
    </div>
    <contact-me />
  </div>
</template>

<script>
import contactMe from '~/components/contact-me.vue'
export default {
  components: { contactMe }
}
</script>

<style>
.dp {
  border-radius: 50%;
  max-width: 13rem;
  margin-bottom: 2%;
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

</style>
