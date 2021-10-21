<template>
  <div class="home">
     <section >  
        <b-button v-on:click="hi">Div 1</b-button>
        <br/>
        <div id="div1" class="div" ref="div1">This is Div 1</div>
        <div id="div2" class="div" ref="div2">This is Div 2</div>
        <div id="div3" class="div" ref="div3">This is Div 3</div>
    </section>   
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue';
import { ParticlesBg } from "particles-bg-vue";

export default {
  name: 'Home',
  components: {
    // HelloWorld,
    ParticlesBg,
  },
  methods:{

    hi() {
        console.log('hi');
    },
  },
}
</script>
<style lang="scss">
button{
  margin-top:150px;
}

.div {
  height: 1000px;
  padding: 20px;
  border: 2px solid yellow;
}
</style>
