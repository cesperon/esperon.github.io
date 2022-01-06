<template>
  <div class="popup">
    <div class="popup-inner" data-aos="flip-up" data-aos-delay="200" data-aos-easing="ease-in">
        <div class="card">
          <div class="cardImg">
            <b-button class="changeImgLeft" @click="increment(-1)" variant="primary"><-</b-button>
            <div>
              <img v-if="imgIndex == 0" class="card-img-top" src="@/assets/screen5.png" alt="Card image cap">
              <img v-if="imgIndex ==1" class="card-img-top" src="@/assets/screen1.png" alt="Card image cap">
              <img v-if="imgIndex ==2" class="card-img-top" src="@/assets/screen4.png" alt="Card image cap">
              <img v-if="imgIndex ==3" class="card-img-top" src="@/assets/screen2.png" alt="Card image cap">
              <img v-if="imgIndex ==4" class="card-img-top" src="@/assets/screen3.png" alt="Card image cap">
            </div>
            <b-button class="changeImgRight" @click="increment(1)" variant="primary" >-></b-button>
          </div>
          <div class="card-body">
            <b>More Information</b>
            <p class="card-text">Gone are the days of using excel sheets to keep track of companies that
            you've applied too. Resume Track is a full stack application that helps organize this data
            and provides insightful information to help you land your next job. Resume track is a form based
            application that helps you keep track of company's hiring managers,their required tech stack,
            compensation and much more.Features like our top stack information can help you see which langauges and frameworks are most common among the jobs you've applied to. Easily visualize data with informative charts and raw numbers.</p>
            <p><b>built with:  </b>
              <img class="stack-img" id="node" alt="App logo" src="@/assets/node.svg">|
              <img class="stack-img" id="sequelize" alt="App logo" src="@/assets/sequelize.svg">|
              <img class="stack-img" id="postgres" alt="App logo" src="@/assets/postgres.svg">|
              <img class="stack-img" id="vue" alt="App logo" src="@/assets/logo.png">|
              <img class="stack-img" id="javascript" alt="App logo" src="@/assets/javascript.svg">|
            </p>
            <p><b>key technical features: </b>
              token authorization flow | frontend state management | object relational mapping | styling with scss
            </p>
            <div class="links">
              Links:
              <p><a href="https://github.com/cesperon/resume_track_frontend">Frontend SRC Code</a></p>
              <p><a href="https://github.com/cesperon/resume_track">Backend SRC Code</a></p>
            </div>
            <b-button class="close mt-0" @click="closePopUp" variant="primary">close</b-button> 
          </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Popup',
  components: {

  },
  data() {
    return {
       openModal: false,
       imgIndex:0,

    };
  },
  methods: {
    openRegister() {
      this.openModal = !this.openModal;
    },
    closePopUp() {
      this.$emit('clicked', 'resume');
    },
    //handle counter for image gallery
    increment(int){
      if(this.imgIndex >= 0 && this.imgIndex <= 4){
        if(this.imgIndex == 0 && int > 0 || this.imgIndex == 4 && int < 0 || this.imgIndex > 0 && this.imgIndex < 4)
        {
            this.imgIndex += int;
        }

      }
      console.log(this.imgIndex);
    },
  },

};
</script>
<style lang="scss">
.popup{
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 99;
  background-color: rgba(0,0,0,0.2);
  display: flex;
  align-items:center;
  justify-content: center;


  .popup-inner {
    background: white;
    // padding: 32px;
    width:700px;
    height:700px;
    border-radius:10px;
    padding-top:0;
    box-shadow: 8px 8px 6px #888888;


  }
  .changeImgRight{
    position:absolute;
    top:0;
    right:0;
    margin-top:120px;
    margin-right:10px;
  }
  .changeImgLeft{
    position:absolute;
    top:0;
    left:0;
    margin-top:120px;
    margin-left:10px;
  }
  .stack-img{
    height:20px;
  }

}
</style>