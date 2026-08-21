<template>
  <section id="home" class="home section">
    <v-row>
      <v-col cols="12" md="4">
        <div class="hero-visual">
          <v-img src="/syahraazly.png" contain max-height="520" alt="Syahraazly illustration"></v-img>
        </div>
        <div class="profile-meta">
          <h2>Syahra Zulya</h2>
          <p>@syahraazly</p>
          <span><i></i> Available for collaboration</span>
        </div>
      </v-col>
      <v-col cols="12" md="8">
        <div class="readme-bar">
          <span><v-icon size="16">mdi-book-open-variant</v-icon> README.md</span>
          <span>···</span>
        </div>
        <article class="text">
          <div class="eyebrow"><span>main</span> / README.md</div>
          <h1>Hi, I'm Syahra <span class="wave">👋</span></h1>
          <h6>Software Developer · Product Explorer · iOS Learner</h6>
          <p>Based in Jakarta, Indonesia. I'm a software engineer transitioning from frontend to fullstack
            development, with professional experience building web applications using Next.js, Vue.js, and
            Tailwind CSS. I'm currently expanding my product development and iOS skills at the Apple Developer
            Academy @ UC, Jakarta.</p>
          <div class="terminal-line"><span>$</span> currently_building --human-centered-products <b>█</b></div>
          <div class="social">
            <a href="https://www.linkedin.com/in/syahraazly" target="_blank">
              <i class='fab fa-linkedin'></i> LinkedIn
            </a>
            <a href="https://github.com/syahraazly" target="_blank"><i class="fab fa-github"></i> GitHub</a>
          </div>
          <a class="download" href="/CV_2024.pdf" download><v-icon size="17">mdi-download</v-icon> Download CV</a>
        </article>
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
  margin-top: 0;
  padding-top: 7.5rem;
  padding-bottom: 2rem;
}

.text {
  color: var(--text);
  animation: reveal-up .8s ease both;
}

.text h1 {
  margin: 25px 0 8px;
  font-size: clamp(2rem, 5vw, 3.8rem);
  line-height: 1.1;
  letter-spacing: -.045em;
}

.text h6 {
  margin-bottom: 24px;
  color: var(--muted);
  font-family: var(--font-mono);
}

.text h6 span {
  font-weight: bold;
  font-size: large;
}

.text a {
  font-size: small;
}

.hero-visual {
  position: relative;
  max-width: 290px;
  margin: auto;
  animation: reveal-scale .9s .1s ease both;
  overflow: hidden;
  background: var(--surface-soft);
  border: 1px solid var(--border);
  border-radius: 50%;
}
.profile-meta { max-width: 290px; margin: 20px auto 0; }
.profile-meta h2 { font-size: 1.3rem; }
.profile-meta p { color: var(--muted); font-family: var(--font-mono); }
.profile-meta span { display: block; margin-top: 13px; color: var(--muted); font-size: .78rem; }
.profile-meta i { display: inline-block; width: 9px; height: 9px; margin-right: 6px; border-radius: 50%; background: var(--green); box-shadow: 0 0 0 4px color-mix(in srgb, var(--green) 16%, transparent); }
.readme-bar { display: flex; justify-content: space-between; padding: 11px 16px; color: var(--muted); background: var(--surface-soft); border: 1px solid var(--border); border-bottom: 0; border-radius: 10px 10px 0 0; font-family: var(--font-mono); font-size: .78rem; }
.readme-bar span:first-child { display: flex; align-items: center; gap: 7px; color: var(--text); }
.text { padding: clamp(24px, 5vw, 52px); background: var(--surface); border: 1px solid var(--border); border-radius: 0 0 10px 10px; }
.eyebrow { color: var(--muted); font-family: var(--font-mono); font-size: .75rem; }
.eyebrow span { color: var(--accent); }
.wave { display: inline-block; animation: wave 2.4s ease-in-out infinite; transform-origin: 70% 70%; }
.terminal-line { margin: 27px 0 20px; padding: 13px 15px; overflow-x: auto; color: var(--muted); background: var(--code); border: 1px solid var(--border); border-radius: 7px; font-family: var(--font-mono); font-size: .78rem; white-space: nowrap; }
.terminal-line span { color: var(--green); }
.terminal-line b { color: var(--accent); animation: blink 1s steps(1) infinite; }
.social { display: flex; flex-wrap: wrap; gap: 9px; margin-bottom: 10px; }
.social a, .download { display: inline-flex; align-items: center; gap: 7px; padding: 8px 12px; color: var(--text); background: var(--surface-soft); border: 1px solid var(--border); border-radius: 6px; font-family: var(--font-mono); font-size: .76rem; transition: .2s ease; }
.social a:hover, .download:hover { color: var(--accent); border-color: var(--accent); transform: translateY(-2px); }
@keyframes wave { 0%, 60%, 100% { transform: rotate(0); } 10% { transform: rotate(14deg); } 20% { transform: rotate(-8deg); } 30% { transform: rotate(12deg); } 40% { transform: rotate(-4deg); } }
@keyframes blink { 50% { opacity: 0; } }
@keyframes reveal-up { from { opacity: 0; transform: translateY(28px); } }
@keyframes reveal-scale { from { opacity: 0; transform: scale(.92); } }

@media (max-width: 768px) {
  .home { min-height: auto; margin-top: 0; padding-top: 6rem; padding-bottom: 1rem; text-align: left; }
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
  .hero-visual { max-width: 210px; }
  .profile-meta { max-width: 100%; text-align: center; margin-bottom: 34px; }
  .readme-bar { padding-inline: 12px; }
  .text { padding: 24px 18px; }
  .text p { line-height: 1.7; }
  .terminal-line { margin-top: 22px; font-size: .7rem; }
  .social { gap: 7px; }
  .social a, .download { flex: 1 1 auto; justify-content: center; }
}

@media (max-width: 380px) {
  .home { padding-top: 5.5rem; }
  .hero-visual { max-width: 175px; }
  .text h1 { font-size: 1.75rem; }
  .text h6 { font-size: .78rem; line-height: 1.6; }
  .terminal-line { margin-inline: -6px; }
}
</style>
