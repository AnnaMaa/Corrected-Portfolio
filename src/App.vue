<template>
  <div id="app">
    <Header />
    <router-view /> 
    <About />
    <Projects />
    <Contact />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import About from "./views/About.vue";
import Contact from "./views/Contact.vue";
import Projects from "./views/Projects.vue";

export default {
  components: {
    Header,
    Footer,
    About,
    Contact,
    Projects,
   
  }
};
</script>

<style>

:root {
    --bg-color: #1f242d;
    --second-bg-color : #323946;
    --text-color : #fff;
    --main-color : #0ef;

}
html {
overflow-x: hidden;
}
</style>
