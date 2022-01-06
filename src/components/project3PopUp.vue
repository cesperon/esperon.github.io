<template>
  <div class="popup">
    <div class="popup-inner" data-aos="flip-up" data-aos-delay="200" data-aos-easing="ease-in">
        <div class="card">
          <div class="cardImg">
            <b-button class="changeImgLeft" @click="increment(-1)" variant="primary"><-</b-button>
            <div>
              <img class="card-img-top" src="@/assets/python.jpg" alt="Card image cap">
            </div>
            <b-button class="changeImgRight" @click="increment(1)" variant="primary" >-></b-button>
          </div>
          <div class="card-body">
            <b>More Information</b>
            <p class="card-text">Python Interpreter written in C++ that follows Python grammar rules, stores variables in global symbol table and evaluates expressions in post fix order.Supports python 2.7
            syntax including and not limited to for loops, while loops, variable declaration and function 
            definitions.</p>
            <p><b>built with:  </b>
              <img class="stack-img" id="node" alt="App logo" src="@/assets/c++.svg">
            </p>
            <div class="links">
              Links:
              <p><a href="https://github.com/cesperon/Python-Interpreter">SRC Code</a></p>
            </div>     
            <b-button class="close mt-0" @click="closePopUp" variant="primary">close</b-button> 
          </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Popup3',
  components: {

  },
  data() {
    return {
       openModal: false,
       // imgIndex:0,

    };
  },
  methods: {
    openRegister() {
      this.openModal = !this.openModal;
    },
    closePopUp() {
      this.$emit('clicked', 'python');
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

}
</style>