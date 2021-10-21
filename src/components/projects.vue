<template>
  <div class="container">
    <div class="projects mx-auto">
      <h2 class="projectsHeader mb-4" data-aos="fade-down-right" data-aos-delay="600" data-aos-easing="ease-in">Projects</h2>
        <div class="row">
            <div class="column col-md-4 col-sm-12" data-aos="fade-down-right" data-aos-delay="400" data-aos-easing="ease-in" @mouseover="hover = true" @mouseleave="hover=false">
              <div v-if="hover">
                  <b-button data-aos="flip-right" data-aos-delay="200" data-aos-easing="ease-in"> Hllo</b-button>
                  <p data-aos="zoom-in" data-aos-delay="200" data-aos-easing="ease-in">Resume Track is an app that solves the problem of using excel sheets to store app data</p>
              </div>
   
            </div>
            <div class="column col-md-4 col-sm-12" data-aos="fade-down" data-aos-delay="400" data-aos-easing="ease-in">
     
            </div>
            <div class="column col-md-4 col-sm-12" data-aos="fade-down-left" data-aos-delay="400" data-aos-easing="ease-in">

            </div>
        </div>
        <div class="row">
            <div class="column col-md-4 col-sm-12" data-aos="fade-right" data-aos-delay="400" data-aos-easing="ease-in">
       
            </div>
            <div class="column col-md-4 col-sm-12" data-aos="fade-down" data-aos-delay="400" data-aos-easing="ease-in">
        
            </div>
            <div class="column col-md-4 col-sm-12" data-aos="fade-left" data-aos-delay="400" data-aos-easing="ease-in">

            </div>
        </div>
        <div class="row">
            <div class="column col-md-4 col-sm-12" data-aos="fade-up-right" data-aos-delay="400" data-aos-easing="ease-in">
   
            </div>
            <div class="column col-md-4 col-sm-12" data-aos="fade-up-left" data-aos-delay="400" data-aos-easing="ease-in">
    
            </div>
            <div class="column col-md-4 col-sm-12" data-aos="fade-up" data-aos-delay="400" data-aos-easing="ease-in">
            </div>
        </div>
    </div>
  </div>
</template>

<script>
import chart from "@/components/aboutChart.vue"
import { ParticlesBg } from "particles-bg-vue";

  export default {
    components: {
        chart,
        ParticlesBg,
    },
    data() {
      return {
          hover:false,
      };
    },

  }
</script>
<style lang="scss">
@import '../assets/_shared.scss';
.projects{
  width:800px;
  // height:500px;
}
.column {
  width: 33.33%;
  height:200px;
  background:$blue;
  border:.5px solid black;
}
.column:hover{
    box-shadow: 8px 8px 6px #888888;
    background:white;
    // margin-right:2px;
    // margin-left:2px;
}    
</style>