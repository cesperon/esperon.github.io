<template>
  <div id="app">
    <particles-bg color="#112031" type="cobweb" :bg="true" />
     <header>
<!--         <navbar></navbar> -->
      </header>
      <section>

        <p class="hello fw-bold">Hello, I'm <span data-aos="fade-up" data-aos-delay="500" data-aos-easing="ease-in" class="name">Christian Esperon</span><p class="inLetter fw-bold">and I like to build things. </p></p>
        <b-button data-aos="fade-up-right" data-aos-delay="650" data-aos-easing="ease-in" class="scrollB fw-bold" @click="hi">View my work <b-icon icon="capslock"></b-icon></b-button>
      </section>
      <div id="div1" class="div" ref="div1">
        <!-- <about class="about"></about> -->
      </div>
      <div id="div2" class="div" ref="div2">
        <about class="about"></about>

      </div>
      <div id="div3" class="div" ref="div3"></div>      
<!--       <router-view/> -->


    </div>
</template>

<script>
// hi
import { ParticlesBg } from "particles-bg-vue";
import navbar from "@/components/Navbar.vue";
import about from "@/components/HelloWorld.vue"
export default {
  components: {
    navbar,
    ParticlesBg,
    about,
  },
  computed: {
      scrollPosition: function() {
          return this.scrollTop;
      },
  },
  created(){
      window.addEventListener('scroll', this.handleScroll);
  },
  methods:{
    handleScroll(event){
      //get rid
      console.log(event);

    },
    goto(){
      // var element = this.$refs[refName];
      // var top = element.offsetTop;

      // window.scrollTo(0, top);
      // const element = document.getElementById('div3');
      // element.scrollIntoView({behavior: 'smooth'});
        console.log('hi');
    },
    hi() {
      const element = document.getElementById('div2');
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
    margin-top:0;
  }

  .scrollB:hover{
      border:3px solid black;
      font-size:28px;
      width:300px;

  }
  .div {
    height: 1000px;
    padding: 20px;
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


}



</style>
