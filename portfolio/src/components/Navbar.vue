<template>
   <div id="nav">
        <nav class="navbar navbar-expand-lg navbar-dark" style="background-color: transparent;">
          <div class="circle mx-2 ms-3">
              <a class="navbar-brand fw-bold" href="#">CE</a>
          </div>
<!--           <img class="linkImage mx-2 clickable" alt="App logo" src="../assets/link.svg">
          <img class="gitImage mx-2" alt="App logo" src="../assets/git.svg">       -->        
          <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
            <div class="navbar-nav me-auto ">
              <a class="nav-item nav-link mx-2 fw-bold" href="#" @click="hi">ABOUT</a>
              <a class="nav-item nav-link mx-2 fw-bold" href="#">PROJECTS</a>
              <a class="nav-item nav-link mx-2 fw-bold" href="#">BLOG</a>
              <a class="nav-item nav-link mx-2 me-5 fw-bold" href="#">CONTACT</a>
            </div>
          </div>
        </nav>
    </div>
</template>


<script>


export default {
  name: "Navbar",
  components: {
    // HelloWorld,

  },
  methods:{

  },
}
</script>



<style lang="scss">
@import '../assets/_shared.scss';

// body{
//   background-image:url("./assets/train.jpg");
//   background-repeat: no-repeat;
//   background-position:center;
//   // background-size:cover;


// }
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;


}


#nav {

  // overflow: hidden;
  // position: fixed; /* Set the navbar to fixed position */
  // top: 0;  Position the navbar at the top of the page 
  // width: 100%; /* Full width */
  height:100%;  
  margin-top:0;
  background:#091353  ;

  .navbar{
    .navbar-nav{
      font-family:$default_font;
      font-size:30px;

    }
    .navbar-brand{
      color:black;
    }
    border:1px solid black;
     box-shadow: 8px 8px 6px #888888;
     .navbar-brand{
        font-family: $default_font2;
        color:$blue1;
        font-size:26px;
     }
     .circle {
        border-radius: 50%;
        width: 54px;
        height: 60px;
        padding: 8px;


        border: 2px solid $blue1;
        color: #666;
        text-align: center;

    }
     .gitImage{
      height:40px;
      cursor:pointer;
      // background:white;
    }
    .linkImage{
      height:40px;
      width:120px;
      cursor:pointer;
    }
    img:hover,
    img.router-link-active{
      border-bottom: 2px solid $blue1;
    }    a:hover,
    a.router-link-active{
      border-bottom: 2px solid $blue1;
    }
  }

}
</style>
