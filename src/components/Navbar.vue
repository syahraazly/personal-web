<template>
  <div class="navbar">
    <header>
      <a href="#"><span>S</span>YH<span>R</span>Z<span>.</span></a>
      <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#experience">Experience</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>
  </div>
</template>

<script>
export default {
  name: "NavbarView"
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
  padding: 20px 120px;
  background: #dfabbd;
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 9999;
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
  transition: 0.3s;
}
nav a:hover {
  color: #ec5453;
}
</style>