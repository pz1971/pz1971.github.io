<template>
  <div>
    <head />
    <div class="center">
      <img class="dp" src="~/assets/dp.jpg">
      <div class="greeting">Hi! I'm</div>
      <div class="parvez-mia">Parvez Mia</div>
      <div class="pz1971">(pz1971)</div>
    </div>
    <div class="bio">
      <div class="bio-item">Competitive Programmer</div><div class="separator"></div>
      <div class="bio-item">Undergrad Student</div><div class="separator"></div>
      <div class="bio-item">Software Developer</div>
    </div>
  </div>
</template>

<script>
export default {
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
        content: 'n9xiG0RwXxlUsgtmfW7Mf3zoKr-dD-oaYA4VVrWnLyg'
      }
    ]
  }
}
</script>

<style>
:root {
  --medium-font-size: 1.5rem;
  --large-font-size: 2.5rem;
  --small-font-size: 1.2rem;
}

.center {
  margin: auto;
  width: 50%;
  padding: 10px;
  text-align: center;
}

.dp {
  border-radius: 50%;
  max-width: 15rem;
  padding-bottom: 2%;
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
  /* color: #fe4a4b; */
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
  color:crimson;
}
</style>
