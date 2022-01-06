<template>
  <div id="app">
    <particles-bg color="#112031" type="cobweb" :bg="true" /> 
      <section>
      <div class="alert alert-primary" role="alert">
        <h3>Under construction. Some features are currently not working...</h3>
      </div>
        <p class="hello fw-bold">Hello, I'm <span data-aos="fade-up-left" data-aos-delay="500" data-aos-easing="ease-in" class="name">Christian Esperon</span><p class="inLetter fw-bold">and I like to build things. </p></p>
        <b-button data-aos="fade-up-right" data-aos-delay="650" data-aos-easing="ease-in" class="scrollB fw-bold" @click="scrollToDiv('div1')">View my work <b-icon icon="capslock"></b-icon></b-button>
      </section>

      <div v-if="scrollE">
        <navbar :class="{bnav: scrollE }" @clicked="scrollToDiv"></navbar>
      </div>

      <div id="div1" class="container-fluid div" ref="div1">
        <!-- <particles-bg color="#112031" type="cobweb" :bg="true" />  -->
        <!-- <stack class="stack mt-5 pt-4"></stack> -->
<!--         <div class="container">  -->
            <!-- <h2>About Me</h2> -->
            <div class="row main1">
              <about class="about col-4" data-aos="fade-up-right" data-aos-delay="500" data-aos-easing="ease-in"></about>
              <progressBar class="ms-auto pBar col-4" ></progressBar>
            </div> 
<!--         </div> -->
      </div>

      <div id="div2" class="container-fluid div" ref="div2">
        <projects ></projects>
      </div>

      <div id="div3" class="div" ref="div3">

        <contact data-aos="fade-up-right" data-aos-delay="500" data-aos-easing="ease-in"></contact>
      </div>      
<!--       <router-view/> -->
<!--           <contact></contact> -->
      <footer>
          <div class="footer">
            <ul class="foote_bottom_ul_amrc">
            <li><a href="http://webenlance.com">Home</a></li>
            <li><a href="http://webenlance.com">About</a></li>
            <li><a href="http://webenlance.com">Services</a></li>
            <li><a href="http://webenlance.com">Pricing</a></li>
            <li><a href="http://webenlance.com">Blog</a></li>
            <li><a href="http://webenlance.com">Contact</a></li>
            </ul>
            <!--foote_bottom_ul_amrc ends here-->
            <p class="text-center">Copyright @2021 | Designed With by <a href="#">cesperon labs </a></p>

            <ul class="social_footer_ul mb-0">
              <li><a href="http://webenlance.com"><b-icon class="icon" icon="github
  "></b-icon></a></li>
              <li><a href="http://webenlance.com"><i class="fab fa-twitter"></i></a></li>
              <li><a href="http://webenlance.com"><i class="fab fa-linkedin"></i></a></li>
              <li><a href="http://webenlance.com"><i class="fab fa-instagram"></i></a></li>
            </ul>
            <!--social_footer_ul ends here-->
          </div>
        </footer>
            
    </div>
</template>

<script>
import { ParticlesBg } from "particles-bg-vue";
import navbar from "@/components/Navbar.vue";
import about from "@/components/HelloWorld.vue"
import stack from "@/components/techStack.vue"
import chart from "@/components/aboutChart.vue"
import progressBar from "@/components/progressBar.vue"
import contact from "@/components/contactForm.vue"
import projects from "@/components/projects.vue"

import "animate.css";

export default {
  components: {
    navbar,
    ParticlesBg,
    about,
    stack,
    chart,
    progressBar,
    contact,
    projects
  },
  computed: {

  },
  data() {
    return{

      scrollE:null,
      scrollOut: null,
    };
  },
  mounted() {
      this.scrollE = false;

      window.addEventListener('scroll', this.updateScroll);
  },
  methods:{
    updateScroll() {
        console.log(this.scrollE);
        this.scrollP = window.scrollY;
        if(this.scrollP >= 1000){
          this.scrollE = true;
        }else{
          this.scrollE = false;
        }
    },
    scrollToDiv(div) {
      console.log(div, 'from parent')
      const element = document.getElementById(div);
      element.scrollIntoView({behavior: 'smooth'});


    },
  },
}
</script>

<style lang="scss">
@import 'assets/_shared.scss';
// @import "../assets/_shared.scss";
#app {

  font-family:$default_font3;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

  #div2{
    background:white;


  }
  #div1{
    display:flex;
    justify-content: center;
    margin-top:400px;
    background:rgb(238, 240,243);
  
  }
  .scrollB{
    margin-top:0;
    width:250px;
    height:70px;
    border:2px solid black;
    background:transparent;
    font-family:$default_font2;
    font-size:25px;
    color:$blue;
    box-shadow: 8px 8px 6px #888888;

  }
  .pBar{
    width:50%;
    height:55%;
  }
  .main1{
    width:75%;
    margin-top:100px;
  }
  .name{
    color:$blue;
  }
  .hello{
    margin-top:500px;
    font-family:$default_font2;
    font-size:40px;
    font-weight:900;
    color:black;  
    margin-bottom:0;
  }
  .about{
    height:50%;
    width:35%;
  }
  .aboutChart{
    width:600px;  
    margin-right:200px;
    margin-top:20px;
  }

  .scrollB:hover{
      border:3px solid black;
      font-size:28px;
      width:300px;

  }
  .div {
    height: 1200px;
    border: 1px solid transparent;
  }
  .inLetter{
    color:black;
    font-size:40px;
    font-family:$default_font2;
  }

  .bnav{
    animation: mymove .5s ease-in-out;
    @keyframes mymove {
      from {
        top:-60px;
      }
      to {
        top:0;
        }
      }

    position: fixed;
    top: 0;
    width: 100%;
    height:82px;
    z-index: 500 
  }
  .stack{
    margin-top:20px;

  }
  .projectsHeader{
    margin-top:200px;
  }
  #div3{
    margin-top:100px;
        background:rgb(238, 240,243);
  }
  .foote_bottom_ul_amrc {
    list-style-type:none;
    padding:0px;
    display:table;
    margin-top: 10px;
    margin-right: auto;
    margin-bottom: 10px;
    margin-left: auto;
  }
  .foote_bottom_ul_amrc li { display:inline;}
  .foote_bottom_ul_amrc li a { color:#B1E693; margin:0 12px;}  
  .footer{
    padding-bottom:0;

    background:#90AACB;
  }

}

@media only screen and (max-width:500px) {
  #div1{
    margin-bottom:300px;
  }
  #div2{
    margin-bottom:900px;
  }
}



</style>
