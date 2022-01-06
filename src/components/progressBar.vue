<template>
  <div class="progressBar">
    <header class="header"></header>
    <particles-bg color="#112031" type="cobweb" :bg="true" />
    <!--     <h2>Comfortability Chart <b-icon icon="hand-thumbs-up"></b-icon></h2> -->
    <div class="progressCol mb-3">
      <img
        id="javascript"
        alt="App logo"
        src="@/assets/logo.png"
        data-aos="flip-up"
        data-aos-delay="100"
        data-aos-easing="ease-in"
      />
      <b-progress
        height="30px"
        :value="60"
        variant="success"
        :striped="striped"
        :animated="true"
        class="progBar"
        show-progress
        data-aos="fade-up-left"
        data-aos-delay="200"
        data-aos-easing="ease-in"
      ></b-progress>
    </div>

    <div class="progressCol mb-3">
      <img
        id="node"
        alt="App logo"
        src="@/assets/node.svg"
        data-aos="flip-up"
        data-aos-delay="100"
        data-aos-easing="ease-in"
      />
      <b-progress
        height="30px"
        :value="70"
        variant="success"
        :striped="striped"
        :animated="true"
        class="mt-3 progBar"
        show-progress
        data-aos="fade-up-left"
        data-aos-delay="300"
        data-aos-easing="ease-in"
      ></b-progress>
    </div>
    <div class="progressCol mb-3">
      <img
        alt="App logo"
        src="@/assets/javascript.svg"
        data-aos="flip-up"
        data-aos-delay="100"
        data-aos-easing="ease-in"
      />
      <b-progress
        height="30px"
        :value="75"
        variant="success"
        :striped="striped"
        :animated="true"
        class="mt-3 progBar"
        show-progress
        data-aos="fade-up-left"
        data-aos-delay="400"
        data-aos-easing="ease-in"
      ></b-progress>
    </div>
    <div class="progressCol mb-3">
      <img
        id="node"
        alt="App logo"
        src="@/assets/python.svg"
        data-aos="flip-up"
        data-aos-delay="100"
        data-aos-easing="ease-in"
      />
      <b-progress
        height="30px"
        :value="70"
        variant="success"
        :striped="striped"
        :animated="true"
        class="mt-3 progBar"
        show-progress
        data-aos="fade-up-left"
        data-aos-delay="500"
        data-aos-easing="ease-in"
      ></b-progress>
    </div>
    <div class="progressCol mb-3">
      <img
        id="node"
        alt="App logo"
        src="@/assets/c++.svg"
        data-aos="flip-up"
        data-aos-delay="100"
        data-aos-easing="ease-in"
      />
      <b-progress
        height="30px"
        :value="60"
        variant="success"
        :striped="striped"
        :animated="true"
        class="mt-3 progBar"
        show-progress
        data-aos="fade-up-left"
        data-aos-delay="600"
        data-aos-easing="ease-in"
      ></b-progress>
    </div>
    <div class="progressCol mb-3">
      <img
        id="node"
        alt="App logo"
        src="@/assets/postgres.svg"
        data-aos="flip-up"
        data-aos-delay="100"
        data-aos-easing="ease-in"
      />
      <b-progress
        height="30px"
        :value="50"
        variant="success"
        :striped="striped"
        :animated="true"
        class="mt-3 progBar"
        show-progress
        data-aos="fade-up-left"
        data-aos-delay="700"
        data-aos-easing="ease-in"
      ></b-progress>
    </div>
    <div class="progressCol mb-3">
      <img
        id="node"
        alt="App logo"
        src="@/assets/sequelize.svg"
        data-aos="flip-up"
        data-aos-delay="100"
        data-aos-easing="ease-in"
      />
      <b-progress
        height="30px"
        :value="50"
        variant="success"
        :striped="striped"
        :animated="true"
        class="mt-3 progBar"
        show-progress
        data-aos="fade-up-left"
        data-aos-delay="800"
        data-aos-easing="ease-in"
      ></b-progress>
    </div>
    <div class="progressCol">
      <img
        id="node"
        alt="App logo"
        src="@/assets/ts.svg"
        data-aos="flip-up"
        data-aos-delay="100"
        data-aos-easing="ease-in"
      />
      <b-progress
        height="30px"
        :value="75"
        variant="success"
        :striped="striped"
        :animated="true"
        class="mt-3 progBar"
        show-progress
        data-aos="fade-up-left"
        data-aos-delay="900"
        data-aos-easing="ease-in"
      ></b-progress>
    </div>
  </div>
</template>

<script>
import chart from "@/components/aboutChart.vue";
import { ParticlesBg } from "particles-bg-vue";

export default {
  components: {
    chart,
    ParticlesBg,
  },
  data() {
    return {
      striped: true,
    };
  },
};
</script>
<style lang="scss">
.progressBar {
  border: 1px solid black;
  box-shadow: 0 4px 6px 0 rgba(0, 0, 0, 0.3);
  background: white;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.progBar {
  box-shadow: 0 4px 6px 0 rgba(0, 0, 0, 0.3);
  width: 60%;
}
.progressCol {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
h5 {
  text-align: left;
}
img {
  width: 80px;
  height: 40px;

  margin-right: 40px;
}
</style>
