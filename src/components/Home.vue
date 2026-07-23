<template>
  <section id="home" class="home section">
    <v-row>
      <v-col cols="12" md="6">
        <div class="hero-visual">
          <span class="orbit orbit-one"></span>
          <span class="orbit orbit-two"></span>
          <v-img src="/syahraazly.png" contain max-height="520" alt="Syahraazly illustration"></v-img>
        </div>
      </v-col>
      <v-col cols="12" md="6">
        <div class="text">
          <h5>HELLO, <span>MY NAME IS</span></h5>
          <h1>SYAHRA <span>ZULYA</span></h1>
          <h6>I'm a <span>Software Developer</span></h6>
          <p>Based in Jakarta, Indonesia. I'm a software engineer transitioning from frontend to fullstack
            development, with professional experience building web applications using Next.js, Vue.js, and
            Tailwind CSS. I'm currently expanding my product development and iOS skills at the Apple Developer
            Academy @ UC, Jakarta.</p>
          <div class="social">
            <a href="https://www.instagram.com/syahraazly" target="_blank">
              <i class='fab fa-instagram'></i>
            </a>
            <a href="https://www.linkedin.com/in/syahraazly" target="_blank">
              <i class='fab fa-linkedin'></i>
            </a>
          </div>
          <v-btn variant="outlined" class="download">
            <a href="/CV_2024.pdf" download>DOWNLOAD CV</a>
          </v-btn>
        </div>
      </v-col>
    </v-row>
  </section>
</template>
<script>
export default {
  name: 'HomeView',
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({ behavior: "smooth" });
    },
  },
}
</script>
<style>
.home {
  min-height: 100vh;
  display: grid;
  align-items: center;
  padding-top: 9rem;
}

.text {
  color: var(--text);
  animation: reveal-up .8s ease both;
}

.text h5 {
  font-weight: bold;
  letter-spacing: .14em;
  color: var(--muted);
}

.text h5 span {
  color: var(--primary);
}

.text h1 {
  font-weight: bold;
  font-size: 3rem;
  -webkit-text-stroke-width: 2px;
  -webkit-text-stroke-color: var(--text);
  color: var(--primary);
}

.text h1 span {
  color: var(--surface);
}

.text h6 {
  margin-bottom: 3rem;
}

.text h6 span {
  font-weight: bold;
  font-size: large;
}

.text a {
  font-size: small;
}

.social i {
  font-size: 40px;
  color: var(--text);
  transition: color 0.3s ease;
  margin-top: 1rem;
  margin-bottom: 1rem;
  margin-right: 2rem;
}

.social i:hover {
  color: var(--primary);
}

.download {
  border-radius: 50px;
}

.download:hover {
  background: var(--primary);
  color: #ffffff;
  transition: background-color 0.3s ease, transform 0.3s ease;
  transform: translateY(-2px);
}

.hero-visual {
  position: relative;
  max-width: 520px;
  margin: auto;
  isolation: isolate;
  animation: reveal-scale .9s .1s ease both;
}

.hero-visual::before {
  content: "";
  position: absolute;
  inset: 12% 8% 0;
  z-index: -2;
  border-radius: 48% 52% 42% 58%;
  background: linear-gradient(145deg, var(--primary), var(--primary-soft));
  animation: morph 8s ease-in-out infinite;
}

.orbit {
  position: absolute;
  z-index: -1;
  border: 1px solid var(--primary);
  border-radius: 50%;
  opacity: .35;
  animation: spin 14s linear infinite;
}
.orbit::after { content: ""; position: absolute; width: 11px; height: 11px; top: 8%; left: 15%; border-radius: 50%; background: var(--primary); }
.orbit-one { inset: 4% 2% 3%; }
.orbit-two { inset: 13% 10% 8%; animation-direction: reverse; animation-duration: 10s; }

@keyframes morph {
  0%, 100% { border-radius: 48% 52% 42% 58%; transform: rotate(-2deg); }
  50% { border-radius: 58% 42% 55% 45%; transform: rotate(2deg); }
}
@keyframes spin { to { transform: rotate(360deg); } }
@keyframes reveal-up { from { opacity: 0; transform: translateY(28px); } }
@keyframes reveal-scale { from { opacity: 0; transform: scale(.92); } }

/* .download a:hover {
  color: #6871d2;
} */

@media (max-width: 768px) {
  .home { padding-top: 7rem; text-align: center; }
  .text {
    padding: 1.5rem 0 0;
  }

  .text h1 {
    font-size: 2rem;
    -webkit-text-stroke-width: 1px;
  }

  .social i {
    font-size: 30px;
  }

  .download {
    padding: 10px 20px;
  }
  .hero-visual { max-width: 360px; }
}
</style>
