<template>
  <v-app id="home">
    <Navbar />
    <v-container>
      <Home />
  
      <!-- <About /> -->
      <Experience />
      <Project />
      <Contact />
    </v-container>
  </v-app>
</template>

<script>
import { defineComponent } from "vue";

// Components
import Navbar from "../components/Navbar.vue";
import Home from "../components/Home.vue";
// import About from "../components/About.vue";
import Experience from "../components/Experience.vue";
import Project from "../components/Project.vue";
import Contact from "../components/Contact.vue";

export default defineComponent({
  name: "HeroView",
  components: {
    Navbar,
    Home,
    // About,
    Experience,
    Project,
    Contact,
  },
});
</script>