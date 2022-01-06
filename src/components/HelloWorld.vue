<template>
  <div>
    <!--       <h2 class="fw-bold">About</h2> -->
    <div>
      <!-- <img class="profile mx-4" alt="App logo" src="@/assets/chris.jpg" >
            <p class="aboutText mt-4" >I'm a <span class="highlightText">full-stack engineer</span> living in Santa Rosa, Ca 
              <br>with a background in computer science. I'm  
              <br>passionate about building full stack data driven 
              <br>applications.
            </p> -->
      <div class="profile">
        <img src="@/assets/chris.jpg" alt="Card image cap" />
        <div>
          <div class="aboutText">
            <p>
              I'm a
              <span class="highlightText">full-stack engineer</span> living in
              Santa Rosa, Ca. Currenly looking for web engineering positions.
              Experience with early stage start-up working as a software
              engineer.There I was tasked with helping build and scale the
              product for official launch. I worked primarily with Node.js,
              Vue.js, Postgres,Sequelize, AWS s3. A majority of our dataset was
              spatial data, so I have some experience working with GeoJson,
              Postgis and building front-end components to display this data
              including charts, and graphs.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import navbar from "@/components/Navbar.vue";
import "animate.css";
export default {
  name: "HelloWorld",
  components: { navbar },
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/_shared.scss";
.aboutText {
  font-size: 20px;
  font-weight: 500;
  font-family: $default_font;
  // width: 500px;
}
a {
  color: #42b983;
}
.profile {
  // height: 500px;
  // width: 500px;
  // box-shadow: 8px 8px 6px #888888;
  box-shadow: 0 4px 6px 0 rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  background: white;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.highlightText {
  color: $blue;
  font-weight: 900;
}
img {
  height: 600px;
  width: 100%;
  margin: 0;
}
</style>
