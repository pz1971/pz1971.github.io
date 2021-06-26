<template>
  <div class="container">
    <a href="mailto: parvez.pz1971@gmail.com"><img class="social-icon" src="~/assets/social-media-icons/mail-icon.png" alt="email: parvez.pz1971@gmail.com"></a>
    <a href="https://www.linkedin.com/in/pz1971/"><img class="social-icon" src="~/assets/social-media-icons/linkedin-icon.png" alt="linked-in: https://www.linkedin.com/in/pz1971/"></a>
    <a href="https://github.com/pz1971/"><img class="social-icon" src="~/assets/social-media-icons/github-icon.png" alt="github: https://github.com/pz1971/"></a>
    <a href="https://twitter.com/pz_parvez"><img class="social-icon" src="~/assets/social-media-icons/twitter-icon.png" alt="twitter: https://twitter.com/pz_parvez"></a>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.container {
    margin: auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-top: 1ch;
    margin-bottom: 1ch;
}
.social-icon {
  max-width: 3.5rem;
  padding-left: 1ch;
  padding-right: 1ch;
}
.social-icon:hover{
  transform: scale(1.1, 1.1);
}
</style>
