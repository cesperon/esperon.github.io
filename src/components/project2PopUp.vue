<template>
  <div class="popup">
    <div class="popup-inner" data-aos="flip-up" data-aos-delay="200" data-aos-easing="ease-in">
        <div class="card">
          <div class="cardImg">
            <b-button class="changeImgLeft" @click="increment(-1)" variant="primary"><-</b-button>
            <div>
              <img v-if="imgIndex == 0" class="card-img-top" src="@/assets/camp.png" alt="Card image cap">
              <img v-if="imgIndex ==1" class="card-img-top" src="@/assets/camp4.png" alt="Card image cap">
              <img v-if="imgIndex ==2" class="card-img-top" src="@/assets/camp5.png" alt="Card image cap">
              <img v-if="imgIndex ==3" class="card-img-top" src="@/assets/camp3.png" alt="Card image cap">
            </div>
            <b-button class="changeImgRight" @click="increment(1)" variant="primary" >-></b-button>
          </div>
          <div class="card-body">
            <b>More Information</b>
            <p class="card-text">Camp-Find is a social platform for outdoor enthusiasts. Share favorite campsites 
            with other people who have the same passion. Plan your next outdoor adventure around other members
            posts, start conversations in the comment section and keep track of all personal posts in user
            profile section.</p>
             <p><b>built with:  </b>
              <img class="stack-img" id="node" alt="App logo" src="@/assets/node.svg">|
              <img class="stack-img" id="javascript" alt="App logo" src="@/assets/javascript.svg">|
              <img class="stack-img" id="javascript" alt="App logo" src="@/assets/html.svg">|
              <img class="stack-img" id="javascript" alt="App logo" src="@/assets/css.svg">|
            </p>
            <p><b>key technical features: </b>
              session authentication | server-side rendering | fuzzy search | google maps integeration
            </p>
            <div class="links">
              Links:
              <p><a href="https://github.com/cesperon/camp-find">SRC Code</a></p>
            </div>            
            <b-button class="close mt-0" @click="closePopUp" variant="primary">close</b-button> 
          </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Popup2',
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
      this.$emit('clicked', 'camp');
    },
    //handle counter for image gallery
    increment(int){
      if(this.imgIndex >= 0 && this.imgIndex <= 3){
        if(this.imgIndex == 0 && int > 0 || this.imgIndex == 3 && int < 0 || this.imgIndex > 0 && this.imgIndex < 3)
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