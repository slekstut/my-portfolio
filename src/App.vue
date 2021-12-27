<template>
  <div>
    <Navbar />
    <Main />
    <Services />
    <Projects />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Main from "./views/Main.vue";
import Services from "./views/Services.vue";
import Projects from "./views/Projects.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Main,
    Services,
    Projects,
  },
};
</script>

<style lang="scss">
html {
  box-sizing: border-box;
}
*,
*:before,
*:after {
  box-sizing: inherit;
}

body {
  margin: 0;
  padding: 0;
  font-size: $fontSize;
}

#app {
  font-family: $font;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
