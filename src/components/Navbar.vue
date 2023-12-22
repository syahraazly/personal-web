<template>
  <div class="navbar">
    <header>
      <a href="#" style="color: #ffffff"><span>syahraazly</span></a>
      <div class="burger-menu" @click="toggleMenu">
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
      </div>
      <nav ref="navMenu">
        <a href="#home">Home</a>
        <a href="#experience">Experience</a>
        <!-- <a href="#contact">Contact</a> -->
      </nav>
    </header>
  </div>
</template>

<script>
export default {
  name: "NavbarView",
  methods: {
    toggleMenu() {
      this.$refs.navMenu.classList.toggle('is-active');
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
  /* Penyesuaian padding untuk semua ukuran layar */
  background: rgba(0, 0, 0, 0.8);
  /* Background hitam transparan */
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 9999;
  transition: background-color 0.3s;
  /* Transisi background */
}

a {
  font-size: 25px;
  color: #ffffff;
  text-decoration: none;
  font-weight: 600;
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

/* Gaya untuk burger menu */
.burger-menu {
  display: none;
  cursor: pointer;
}

.burger-menu .line {
  width: 25px;
  height: 2px;
  background-color: white;
  margin: 5px 0;
}

/* Gaya ketika di layar mobile */

@media (max-width: 768px) {
  .burger-menu {
    display: block;
  }

   nav {
    display: none;
    position: absolute;
    top: 60px; /* Atur sesuai dengan tinggi navbar */
    left: 0;
    width: 100%;
    background: rgba(0, 0, 0, 0.8); /* Sesuaikan dengan warna navbar */
    transition: all 0.3s ease; /* Animasi untuk menampilkan dan menyembunyikan menu */
  }

  nav.is-active {
    display: block;
  }
}
</style>