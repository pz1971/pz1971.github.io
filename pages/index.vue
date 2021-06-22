<template>
  <div>
    <div class="center">
      <img class="dp" src="~/assets/resources/dp.jpg">
      <div class="greeting">Hi! I'm</div>
      <div class="parvez-mia">Parvez Mia</div>
      <div class="pz1971">(pz1971)</div>
      <div class="bio"><span class="bioTitle">Competitive Programmer</span> || <span class="bioTitle">Undergrad Student</span> || <span class="bioTitle">Web developer</span></div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>

.center {
  margin: auto;
  width: 50%;
  padding: 10px;
  text-align: center;
}

.dp {
  border-radius: 50%;
  max-width: 250px;
}

.greeting {
  font-size: 1.5rem;
  font-family: monospace;
}
.parvez-mia {
  font-weight: bold;
  font-size: 2.5rem;
  font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
}
.pz1971 {
  font-size: 1.5rem;
  font-family: monospace;
}
.pz1971:hover {
  /* color: #fe4a4b; */
  transform: rotate(10deg);
}
.bio {
  font-size: 1.5rem;
  font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.bioTitle:hover{
  display: inline-block;
  transform: scale(1.05, 1.05);
}

</style>
