<template>
  <div>
    <div class="outer-wrapper">
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
    <hr class="horizontal-line">
    <!-- education section -->
    <div class="section">
      <h2>
        Skills
      </h2>
    </div>
    <div class="section">
      <h2>
        Education
      </h2>
      <ul>
        <li>
          Ahsanullah University of Science and Technology (<a href="https://www.aust.edu/">AUST</a>)
          <ul>
            <li>
              Doing B.Sc(Engg.) in Computer Science and Engineering
            </li>
            <li>
              Expected Graduation time: November, 2022
            </li>
          </ul>
        </li>
      </ul>
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
.outer-wrapper {
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
.horizontal-line {
  margin: 2% 20%;
}
.section {
  margin-left: 20%;
  margin-right: 20%;
}

</style>
