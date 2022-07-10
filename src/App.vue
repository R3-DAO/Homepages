<template>
  <div id="app">
    <el-container style="">
      <el-header>
        <img style="" src="./assets/imgs/logo.png" alt />
      </el-header>
      <el-main>
        <router-view />
      </el-main>
    </el-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      router: true,
    };
  },
  methods: {},
};
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
}
html,
body {
  height: 100%;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

.el-header {
  display: flex;
  justify-content: space-between;
  align-content: center;
  width: 1240px;
  margin: 0 auto;
  height: 100px !important;
  width: 100%;
  background-image: linear-gradient(#5324f2, #3e16f4);
  img {
    height: 100px !important;
    margin-left: 200px;
  }
}

.el-main {
  padding: 0 !important;
}
</style>
