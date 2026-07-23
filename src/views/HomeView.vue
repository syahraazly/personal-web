<template>
  <div class="site-shell">
    <Navbar :is-dark="isDark" @toggle-theme="toggleTheme" />
    <main>
      <Home />
      <Experience />
      <Project />
      <Contact />
    </main>
  </div>
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
  data() {
    return {
      isDark: false,
    };
  },
  created() {
    const savedTheme = localStorage.getItem("syahraazly-theme");
    const prefersDark = window.matchMedia("(prefers-color-scheme: dark)").matches;
    this.isDark = savedTheme ? savedTheme === "dark" : prefersDark;
    this.applyTheme();
  },
  methods: {
    applyTheme() {
      document.documentElement.dataset.theme = this.isDark ? "dark" : "light";
    },
    toggleTheme() {
      this.isDark = !this.isDark;
      localStorage.setItem("syahraazly-theme", this.isDark ? "dark" : "light");
      this.applyTheme();
    },
  },
});
</script>
