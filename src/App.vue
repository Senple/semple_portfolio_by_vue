<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">About</router-link>|
      <router-link to="/skill">Skill</router-link>|
      <router-link to="/travel">Travel</router-link>|
      <router-link to="/contact">Contact</router-link>
    </div>
    <router-view />
  </div>
</template>

<script>
// import Loading from "./components/Loading.vue";

// export default {
//   name: "app",
//   data() {
//     return {
//       loading: true
//     };
//   },
//   mounted() {
//     console.log("mount start");
//     setTimeout(() => {
//       this.loading = false;
//     }, 3000);
//     console.log("mounted");
//   },
//   components: {
//     Loading
//   }
// };
//
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
body {
  background: rgba(194, 229, 252, 0.7);
}

#nav {
  padding: 30px;
  display: block;
  margin: 0 auto;
  /* position: absolute; */
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.selector-for-some-widget {
  box-sizing: content-box;
}
</style>
