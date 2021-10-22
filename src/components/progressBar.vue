<template>
  <div class="progressBar">
<!--     <h2>Comfortability Chart <b-icon icon="hand-thumbs-up"></b-icon></h2> -->
    <h5 data-aos="fade-up-left" data-aos-delay="200" data-aos-easing="ease-in">Vue.js</h5>
    <b-progress height="30px" :value="25" variant="success" :striped="striped" :animated="true" class="progBar" show-progress data-aos="fade-up-left" data-aos-delay="200" data-aos-easing="ease-in"></b-progress>
    <h5  data-aos="fade-up-left" data-aos-delay="300" data-aos-easing="ease-in">Node.js</h5>
    <b-progress height="30px" :value="50" variant="success" :striped="striped" :animated="true" class="mt-3 progBar" show-progress data-aos="fade-up-left" data-aos-delay="300" data-aos-easing="ease-in"></b-progress>
    <h5 data-aos="fade-up-left" data-aos-delay="400" data-aos-easing="ease-in">Javascript</h5>
    <b-progress height="30px" :value="75" variant="success" :striped="striped" :animated="true" class="mt-3 progBar" show-progress data-aos="fade-up-left" data-aos-delay="400" data-aos-easing="ease-in"></b-progress>
    <h5 data-aos="fade-up-left" data-aos-delay="500" data-aos-easing="ease-in">Python</h5>
    <b-progress height="30px" :value="100" variant="success" :striped="striped" :animated="true" class="mt-3 progBar" show-progress data-aos="fade-up-left" data-aos-delay="500" data-aos-easing="ease-in"></b-progress>
    <h5 data-aos="fade-up-left" data-aos-delay="600" data-aos-easing="ease-in">C++</h5>
    <b-progress height="30px" :value="25" variant="success" :striped="striped" :animated="true" class="mt-3 progBar" show-progress data-aos="fade-up-left" data-aos-delay="600" data-aos-easing="ease-in"></b-progress>
    <h5  data-aos="fade-up-left" data-aos-delay="700" data-aos-easing="ease-in">R</h5>
    <b-progress height="30px" :value="50" variant="success" :striped="striped" :animated="true" class="mt-3 progBar" show-progress data-aos="fade-up-left" data-aos-delay="700" data-aos-easing="ease-in"></b-progress>
    <h5  data-aos="fade-up-left" data-aos-delay="800" data-aos-easing="ease-in">Postgres</h5>
    <b-progress height="30px" :value="75" variant="success" :striped="striped" :animated="true" class="mt-3 progBar" show-progress data-aos="fade-up-left" data-aos-delay="800" data-aos-easing="ease-in"></b-progress>
    <h5 data-aos="fade-up-left" data-aos-delay="900" data-aos-easing="ease-in">Data Structures/ Alogrithms</h5>
    <b-progress height="30px" :value="100" variant="success" :striped="striped" :animated="true" class="mt-3 progBar" show-progress data-aos="fade-up-left" data-aos-delay="900" data-aos-easing="ease-in"></b-progress>
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
        striped: true
      };
    },

  }
</script>
<style lang="scss">
.progressBar{
  width:600px;
}
.progBar{
    box-shadow: 0 4px 6px 0 rgba(0, 0, 0, 0.3);
  }
h5{
  text-align:left;
}

</style>