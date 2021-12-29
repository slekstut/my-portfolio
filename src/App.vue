<template>
  <div>
    <Navbar />
    <Main />
    <Services />
    <Projects />
    <Skills />
    <About />
    <Contact />
    <Footer />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Main from "./views/Main.vue";
import Services from "./views/Services.vue";
import Projects from "./views/Projects.vue";
import Skills from "./views/Skills.vue";
import About from "./views/About.vue";
import Contact from "./views/Contact.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Main,
    Services,
    Projects,
    Skills,
    About,
    Contact,
    Footer,
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
  overflow-x: hidden;
}

#app {
  font-family: $font;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
