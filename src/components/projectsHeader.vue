<template>
  <div id="projTools">
    <nav>
      <ul class="toolSearch">
        <h2>Built With:</h2>
        <li><img src="../assets/c++.svg" alt="" /></li>
        <li><img src="../assets/javascript.svg" alt="" /></li>
        <li><img src="../assets/logo.png" alt="" /></li>
        <li><img src="../assets/postgres.svg" alt="" /></li>
        <li><img src="../assets/node.svg" alt="" /></li>
        <li><img src="../assets/ts.svg" alt="" /></li>
      </ul>
    </nav>
  </div>
</template>
<script>
export default {
  name: "projectTools",
  components: {},
  methods: {},
};
</script>

<style lang="scss">
@import "../assets/_shared.scss";
.toolSearch {
  display: flex;
  flex-direction: row;
  justify-content: center;
  list-style-type: none;
  align-items: center;
}
#projTools {
  margin-top: 100px;
  margin-bottom: 30px;
}
li {
  //   border: 1px solid black;
}
img {
  width: 50px;
}
h2 {
  margin-right: 12px;
}
</style>
