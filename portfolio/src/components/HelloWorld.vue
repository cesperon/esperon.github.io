<template>
  <div class="hello" >
      <h2 class="fw-bold">About</h2>
        <div class="d-flex">
          <img class="profile mx-4" alt="App logo" src="@/assets/chris.jpg" >
          <p class="aboutText mt-4" >I'm a <span class="highlightText">full-stack engineer</span> living in Santa Rosa, Ca 
            <br>with a background in computer
            <br>science. I'm passionate about building full stack data driven 
            <br>applications.
          </p>
        </div>
  </div>
</template>

<script>
import navbar from "@/components/Navbar.vue";
import "animate.css";
export default {
  name: 'HelloWorld',
  components: { navbar },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/_shared.scss';
.aboutText{

  font-size:20px; 
  font-family:$default_font;
}
h3 {
  margin: 40px 0 0;
}
h2 {
  text-decoration:underline;
  padding-bottom:10px;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.profile{
  height:500px;
  width:500px;
  // box-shadow: 8px 8px 6px #888888;
  box-shadow: 0 4px 6px 0 rgba(0, 0, 0, 0.3);
  border-radius:10px;
}
.highlightText{
  color:$blue;
  font-weight:900;
}


</style>
