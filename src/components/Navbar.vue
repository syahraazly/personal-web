<template>
  <div class="navbar">
    <header>
      <a href="#" style="color: #ffffff"><span>syahraazly</span></a>
      <!-- Hamburger Menu -->
      <div class="burger-menu" @click="toggleMenu">
        <div :class="{ 'line': true, 'rotate-line1': isMenuActive }"></div>
        <div :class="{ 'line': true, 'hide-line2': isMenuActive }"></div>
        <div :class="{ 'line': true, 'rotate-line3': isMenuActive }"></div>
      </div>
      <!-- Menu Items -->
      <nav :class="{ 'is-active': isMenuActive }">
        <a href="#home">Home</a>
        <a href="#experience">Experience</a>
        <a href="#project">Portfolio</a>
      </nav>
    </header>
  </div>
</template>

<script>
export default {
  name: "NavbarView",
  data() {
    return {
      isMenuActive: false
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuActive = !this.isMenuActive;
    }
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  scroll-behavior: smooth;
}

header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  padding: 20px 40px;
  background: rgba(0, 0, 0, 0.8);
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 9999;
  transition: background-color 0.3s;
}

a {
  font-size: 25px;
  color: #ffffff;
  text-decoration: none;
  font-weight: 600;
}

nav {
  display: none;
  /* Hidden by default for mobile */
  flex-direction: column;
  justify-content: center;
  align-items: center;
  position: absolute;
  top: 100%;
  right: 0;
  background-color: rgba(0, 0, 0, 0.8);
  width: 100%;
  height: 100vh;
  transform: translateX(100%);
  transition: transform 0.5s ease;
}

nav.is-active {
  display: flex;
  transform: translateX(0);
}

nav a {
  font-size: 18px;
  color: #ffffff;
  text-decoration: none;
  font-weight: 500;
  margin-left: 2rem;
  transition: color 0.3s;
}

nav a:hover {
  color: #6871d2;
}

/* Hamburger Menu */
.burger-menu {
  cursor: pointer;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 24px;
  width: 30px;
}

.line {
  width: 30px;
  height: 3px;
  background-color: #fff;
  transition: all 0.3s ease;
}

/* Hamburger Animations */
.rotate-line1 {
  transform: rotate(45deg) translate(5px, 5px);
}

.hide-line2 {
  opacity: 0;
}

.rotate-line3 {
  transform: rotate(-45deg) translate(5px, -5px);
}

/* Responsive Styling for Mobile */
@media (max-width: 768px) {
  nav {
    position: absolute;
    top: 100%;
    right: 0;
    background-color: rgba(0, 0, 0, 0.8);
    width: 100%;
    height: 100vh;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    transform: translateX(100%);
  }

  nav.is-active {
    transform: translateX(0);
  }
}

/* Styling for Desktop */
@media (min-width: 768px) {
  .burger-menu {
    display: none;
    /* Hide hamburger on desktop */
  }

  nav {
    display: flex;
    /* Show navigation on desktop */
    position: static;
    flex-direction: row;
    background-color: transparent;
    width: auto;
    height: auto;
    transform: none;
  }

  nav a {
    margin-left: 2rem;
  }
}
</style>