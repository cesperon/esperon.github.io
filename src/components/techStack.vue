<template>
  <div class="stack container">
    <div class="row">
      <div v-if="currently" class="stackImg col-12">
        <h2 class="stackHeader">
          Currently Using<b-button
            class="changeViewLeft mx-4 mt-0"
            @click="changeViewLeft"
            ><b-icon class="icon" icon="arrow-left"></b-icon
          ></b-button>
        </h2>
        <img
          class="mx-4"
          id="vue"
          alt="App logo"
          src="@/assets/logo.png"
          data-aos="fade-up-left"
          data-aos-delay="100"
          data-aos-easing="ease-in"
        />|
        <img
          class="mx-4"
          id="node"
          alt="App logo"
          src="@/assets/node.svg"
          data-aos="fade-up-left"
          data-aos-delay="200"
          data-aos-easing="ease-in"
        />|
        <img
          class="mx-4"
          id="sequelize"
          alt="App logo"
          src="@/assets/sequelize.svg"
          data-aos="fade-up-left"
          data-aos-delay="300"
          data-aos-easing="ease-in"
        />|
        <img
          class="mx-4"
          id="postgres"
          alt="App logo"
          src="@/assets/postgres.svg"
          data-aos="fade-up-left"
          data-aos-delay="400"
          data-aos-easing="ease-in"
        />
        <!-- 
            tooltips for images -->
        <b-tooltip target="postgres" variant="primary" triggers="hover">
          <b>Postgres</b>
        </b-tooltip>
        <b-tooltip target="vue" variant="primary" triggers="hover">
          <b>Vue.js</b>
        </b-tooltip>
        <b-tooltip target="node" variant="primary" triggers="hover">
          <b>Node.js</b>
        </b-tooltip>
        <b-tooltip target="sequelize" variant="primary" triggers="hover">
          <b>Sequelize ORM(Object Relational Mapping)</b>
        </b-tooltip>
      </div>
      <div v-else>
        <h2 class="stackHeader col-12">
          Experience With<b-button
            class="changeViewRight mx-4 mt-0"
            @click="changeViewRight"
            ><b-icon
              class="icon"
              icon="arrow-right
  "
            ></b-icon
          ></b-button>
        </h2>
        <img
          class="mx-4"
          id="javascript"
          alt="App logo"
          src="@/assets/javascript.svg"
          data-aos="flip-up"
          data-aos-delay="100"
          data-aos-easing="ease-in"
        />|
        <img
          class="mx-4"
          id="vue"
          alt="App logo"
          src="@/assets/logo.png"
          data-aos="flip-up"
          data-aos-delay="200"
          data-aos-easing="ease-in"
        />|
        <img
          class="mx-4"
          id="node"
          alt="App logo"
          src="@/assets/node.svg"
          data-aos="flip-up"
          data-aos-delay="300"
          data-aos-easing="ease-in"
        />|
        <img
          class="mx-4"
          id="c"
          alt="App logo"
          src="@/assets/c++.svg"
          data-aos="flip-up"
          data-aos-delay="400"
          data-aos-easing="ease-in"
        />|
        <img
          class="mx-4"
          id="python"
          alt="App logo"
          src="@/assets/python.svg"
          data-aos="flip-up"
          data-aos-delay="400"
          data-aos-easing="ease-in"
        />|
        <!--             <img class="mx-4" id="sequelize" alt="App logo" src="@/assets/sequelize.svg" data-aos="flip-up" data-aos-delay="300" data-aos-easing="ease-in">| -->
        <img
          class="mx-4"
          id="postgres"
          alt="App logo"
          src="@/assets/postgres.svg"
          data-aos="flip-up"
          data-aos-delay="200"
          data-aos-easing="ease-in"
        />|
        <img
          class="mx-4"
          id="git"
          alt="App logo"
          src="@/assets/git.svg"
          data-aos="flip-up"
          data-aos-delay="100"
          data-aos-easing="ease-in"
        />
        <!-- 
            tooltips for images -->
        <b-tooltip target="javascript" variant="primary" triggers="hover">
          <b>Javascript</b>
        </b-tooltip>
        <b-tooltip target="vue" variant="primary" triggers="hover">
          <b>Vue.js</b>
        </b-tooltip>
        <b-tooltip target="node" variant="primary" triggers="hover">
          <b>Node.js</b>
        </b-tooltip>
        <b-tooltip target="sequelize" variant="primary" triggers="hover">
          <b>Sequelize ORM(Object Relational Mapping)</b>
        </b-tooltip>
        <b-tooltip target="python" variant="primary" triggers="hover">
          <b>Python</b>
        </b-tooltip>
        <b-tooltip target="git" variant="primary" triggers="hover">
          <b>Git Hub version control software</b>
        </b-tooltip>
        <b-tooltip target="c" variant="primary" triggers="hover">
          <b>C++</b>
        </b-tooltip>
        <b-tooltip target="postgres" variant="primary" triggers="hover">
          <b>Postgresql</b>
        </b-tooltip>
      </div>

      <!--       <div class="stackBtn h-25 d-inline-block mt-1">
          <b-button class="changeViewLeft mx-1" @click="changeViewLeft"><b-icon class="icon" icon="arrow-left"></b-icon></b-button>
          <b-button class="changeViewRight" @click="changeViewRight"><b-icon class="icon" icon="arrow-right
  "></b-icon></b-button>

        </div> -->
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue';

export default {
  name: "Stack",
  components: {},
  data() {
    return {
      currently: false,
    };
  },
  methods: {
    changeViewLeft() {
      this.currently = false;
    },
    changeViewRight() {
      this.currently = true;
    },
  },
};
</script>
<style lang="scss">
@import "../assets/_shared.scss";
.stack {
  font-family: $default_font2;
  .stackHeader {
    margin-bottom: 40px;
    font-weight: bold;
    text-decoration: underline;
    font-size: 30px;
  }
  #git {
    height: 70px;
  }
  #javascript {
    height: 70px;
  }
  #vue {
    height: 70px;
  }
  #node {
    height: 70px;
  }
  #sequelize {
    height: 70px;
  }
  #postgres {
    height: 70px;
  }
  #c {
    height: 70px;
  }
  #python {
    height: 70px;
  }

  .changeViewRight {
    border: 1px solid black;
    background: #091353;
    // box-shadow: 8px 8px 6px #888888;
    box-shadow: 0 4px 6px 0 rgba(0, 0, 0, 0.3);
  }
  .changeViewLeft {
    border: 1px solid black;
    background: #091353;
    // box-shadow: 8px 8px 6px #888888;
    box-shadow: 0 4px 6px 0 rgba(0, 0, 0, 0.3);
  }
}
</style>
