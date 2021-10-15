<template>
  <div class="projects">
      <div class="d-flex">
          <div class="column" data-aos="fade-down-right" data-aos-delay="400" data-aos-easing="ease-in" @mouseover="hover = true" @mouseleave="hover=false">
            <div v-if="hover">
                <b-button data-aos="flip-right" data-aos-delay="200" data-aos-easing="ease-in"> Hllo</b-button>
                <p data-aos="zoom-in" data-aos-delay="200" data-aos-easing="ease-in">Resume Track is an app that solves the problem of using excel sheets to store app data</p>
            </div>
 
          </div>
          <div class="column" data-aos="fade-down" data-aos-delay="400" data-aos-easing="ease-in">
   
          </div>
          <div class="column" data-aos="fade-down-left" data-aos-delay="400" data-aos-easing="ease-in">

          </div>
      </div>
      <div class="d-flex">
          <div class="column" data-aos="fade-right" data-aos-delay="400" data-aos-easing="ease-in">
     
          </div>
          <div class="column" data-aos="fade-down" data-aos-delay="400" data-aos-easing="ease-in">
      
          </div>
          <div class="column" data-aos="fade-left" data-aos-delay="400" data-aos-easing="ease-in">

          </div>
      </div>
      <div class="d-flex">
          <div class="column" data-aos="fade-up-right" data-aos-delay="400" data-aos-easing="ease-in">
 
          </div>
          <div class="column" data-aos="fade-up-left" data-aos-delay="400" data-aos-easing="ease-in">
  
          </div>
          <div class="column" data-aos="fade-up" data-aos-delay="400" data-aos-easing="ease-in">

          </div>
      </div>
  </div>
</template>

<script>
import chart from "@/components/aboutChart.vue"

  export default {
    components: {
        chart,
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
.column {
  float: left;
  width: 33.33%;
  height:400px;
  background:$blue;
  border:.5px solid black;
}
.column:hover{
    box-shadow: 8px 8px 6px #888888;
    background:white;
}    
</style>