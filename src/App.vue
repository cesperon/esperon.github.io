<template>
  <div id="app">
    <particles-bg color="#112031" type="cobweb" :bg="true" /> 
      <section>
        <p class="hello fw-bold">Hello, I'm <span data-aos="fade-up-left" data-aos-delay="500" data-aos-easing="ease-in" class="name">Christian Esperon</span><p class="inLetter fw-bold">and I like to build things. </p></p>
        <b-button data-aos="fade-up-right" data-aos-delay="650" data-aos-easing="ease-in" class="scrollB fw-bold" @click="hi">View my work <b-icon icon="capslock"></b-icon></b-button>
      </section>

      <div v-if="scrollE">
        <navbar :class="{bnav: scrollE }" ></navbar>
      </div>

      <div id="div1" class="div" ref="div1">
        <!-- <particles-bg color="#112031" type="cobweb" :bg="true" />  -->
        <stack class="stack mt-5 pt-4"></stack>
        <div class="d-flex">
          <about class="about" data-aos="fade-up-right" data-aos-delay="500" data-aos-easing="ease-in"></about>
          <progressBar class="ms-auto pBar" ></progressBar>
        </div> 

      </div>

      <div id="div2" class="div" ref="div2">
        <projects></projects>
      </div>

      <div id="div3" class="div" ref="div3">

        <contact></contact>
      </div>      
<!--       <router-view/> -->
<!--           <contact></contact> -->
            
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
    hi() {
      const element = document.getElementById('div1');
      element.scrollIntoView({behavior: 'smooth'});


    },
  },
}
</script>

<style lang="scss">
@import 'assets/_shared.scss';


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

  #div2{
    padding-top:0;
    padding-left:0;
    padding-right:0;
  }
  #div1{
    margin-top:400px;
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
    margin-top:40px;
    margin-left:400px;
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
    height: 1000px;
    // padding: 20px;
    border: 1px solid transparent;
  }
  .inLetter{
    color:black;
    font-size:40px;
    font-family:$default_font2;
  }
  .about{
    // margin-top:20px;
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
  .pBar{
      margin-top:40px;
      margin-right:400px;
      padding-bottom:0;
      // box-shadow: 8px 8px 6px #888888;
  }
  .projects{
    margin-top:200px;
  }


}



</style>
