<template>
  <div class="container-fluid">
    <div class="projects mx-auto">
      <h2 class="projectsHeader mb-4" data-aos="fade-down-right" data-aos-delay="600" data-aos-easing="ease-in">Projects</h2>
        <div v-if="popup">
          <popUp @clicked="openModal"></popUp>
        </div>
         <div v-if="popup2">
          <popUp2 @clicked="openModal"></popUp2>
        </div>
         <div v-if="popup3">
          <popUp3 @clicked="openModal"></popUp3>
        </div>             
        <div class="row">
            <div class="column col1 col-md-4 col-sm-12" data-aos="fade-down-right" data-aos-delay="400" data-aos-easing="ease-in" @mouseover="hover = true" @mouseleave="hover=false">
              <div v-if="hover">
                  <p class="prjTxt" data-aos="zoom-in" data-aos-delay="200" data-aos-easing="ease-in">Organize the job search process with Resume Track</p>
                  <b-button @click="openModal('resume')" class="prjBtn" variant="primary" data-aos="flip-right" data-aos-delay="200" data-aos-easing="ease-in">Learn More</b-button>
              </div>
            </div>
            <div class="column col2 col-md-4 col-sm-12" data-aos="fade-down" data-aos-delay="400" data-aos-easing="ease-in" @mouseover="hover2 = true" @mouseleave="hover2=false">
              <div v-if="hover2">
                  <p class="prjTxt" data-aos="zoom-in" data-aos-delay="200" data-aos-easing="ease-in">Camp-Find is a social platform to share camping/hiking locations</p>
                  <b-button @click="openModal('camp')" class="prjBtn" variant="primary" data-aos="flip-right" data-aos-delay="200" data-aos-easing="ease-in">Learn More</b-button>
              </div>
            </div>
            <div class="column col3 col-md-4 col-sm-12" data-aos="fade-down-left" data-aos-delay="400" data-aos-easing="ease-in" @mouseover="hover3 = true" @mouseleave="hover3=false">
              <div v-if="hover3">
                  <p class="prjTxt" data-aos="zoom-in" data-aos-delay="200" data-aos-easing="ease-in">Python Interpreter written in C++</p>
                  <b-button @click="openModal('python')" class="prjBtn" variant="primary" data-aos="flip-right" data-aos-delay="200" data-aos-easing="ease-in">Learn More</b-button>
              </div>

            </div>
        </div>
<!--         <div class="row">
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
        </div> -->
    </div>
  </div>
</template>

<script>
import chart from "@/components/aboutChart.vue"
import { ParticlesBg } from "particles-bg-vue";
import popUp from "@/components/projectPopUp.vue"
import popUp2 from "@/components/project2PopUp.vue"
import popUp3 from "@/components/project3PopUp.vue"

  export default {
    components: {
        chart,
        ParticlesBg,
        popUp,
        popUp2,
        popUp3,
    },
    data() {
      return {
          hover:false,
          hover2:false,
          hover3:false,
          popup: false,
          popup2: false,
          popup3: false,
      };
    },
    methods: {
        openModal(str){
            if(str == 'resume'){
              this.popup = !this.popup;
              console.log('this is resume');
            }
            if(str == 'camp'){
              this.popup2 = !this.popup2;
            }
            if(str == 'python'){
              this.popup3 = !this.popup3;
            }

        },
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
  height:300px;
  border:2px solid black;
  border-radius:10px;
}
.column:hover{
    box-shadow: 8px 8px 6px #888888;
    background:black;
    color:white;
}
.col1::after{
  content: "";
  border-radius:10px;
  background-image:url('../assets/rt.jpg');
  opacity:1;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  position: absolute;
  z-index: -1;   
  background-repeat: no-repeat;
  background-size:300px 300px;
}
.col1:hover::after{
  opacity:0.34;
}

.col2::after{
  content: "";
  border-radius:10px;
  background-image:url('../assets/camp.png');
  opacity:1;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  position: absolute;
  z-index: -1;   
  background-repeat: no-repeat;
  background-size:300px 300px;
}
.col2:hover::after{
  opacity:0.34;
}

.col3::after{
  content: "";
  border-radius:10px;
  background-image:url('../assets/python.jpg');
  opacity:1;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  position: absolute;
  z-index: -1;   
  background-repeat: no-repeat;
  background-size:300px 300px;
}
.col3:hover::after{
  opacity:0.34;
}
.prjBtn{
  margin-top:25px;
}
.prjTxt{
  margin-top:15px;
}

// @media only screen and (max-width:500px) {
//   .column{
//     width:100px
//   }
// }

</style>