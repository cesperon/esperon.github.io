<template>
  <div class="hello">
    <div data-aos="fade-down-right" data-aos-easing="ease-in" data-aos-delay="500">
      <navbar></navbar>
    </div>

  </div>
</template>

<script>
import navbar from "@/components/Navbar.vue";
import "animate.css";
export default {
  name: 'HelloWorld',
  components: { navbar },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
