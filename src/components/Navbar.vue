<template>
  <header class="site-header">
    <a class="brand" href="#home" aria-label="Syahraazly home" @click.prevent="navigate('#home')">
      <v-icon class="github-mark">mdi-github</v-icon>
      <span>syahraazly</span><b>/</b><span class="repo-name">portfolio</span>
    </a>

    <div class="header-actions">
      <button
        class="theme-toggle"
        type="button"
        :aria-label="isDark ? 'Switch to light mode' : 'Switch to dark mode'"
        @click="$emit('toggle-theme')"
      >
        <v-icon>{{ isDark ? "mdi-weather-sunny" : "mdi-weather-night" }}</v-icon>
      </button>
      <button
        class="menu-toggle"
        type="button"
        :class="{ active: isMenuActive }"
        :aria-expanded="isMenuActive"
        aria-label="Toggle navigation"
        @click="toggleMenu"
      >
        <span></span><span></span><span></span>
      </button>
    </div>

    <nav :class="{ active: isMenuActive }">
      <a v-for="item in menuItems" :key="item.href" :href="item.href" @click.prevent="navigate(item.href)">
        {{ item.label }}
      </a>
    </nav>
  </header>
</template>

<script>
export default {
  name: "NavbarView",
  props: {
    isDark: Boolean,
  },
  emits: ["toggle-theme"],
  data() {
    return {
      isMenuActive: false,
      menuItems: [
        { label: "README", href: "#home" },
        { label: "Commits", href: "#experience" },
        { label: "Repositories", href: "#project" },
        { label: "Contact", href: "#contact" },
      ],
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuActive = !this.isMenuActive;
    },
    closeMenu() {
      this.isMenuActive = false;
    },
    navigate(href) {
      this.closeMenu();
      const section = document.querySelector(href);
      if (!section) return;
      const reduceMotion = window.matchMedia("(prefers-reduced-motion: reduce)").matches;
      section.scrollIntoView({ behavior: reduceMotion ? "auto" : "smooth", block: "start" });
      window.history.replaceState(null, "", href);
    },
  },
};
</script>

<style scoped>
.site-header {
  position: fixed;
  inset: 0 0 auto;
  z-index: 1000;
  display: flex;
  align-items: center;
  min-height: 64px;
  padding: 8px var(--page-gutter);
  color: var(--text);
  background: color-mix(in srgb, var(--surface) 92%, transparent);
  border-bottom: 1px solid var(--border);
  backdrop-filter: blur(18px);
}
.brand { display: inline-flex; align-items: center; gap: 7px; color: var(--text); font-size: .95rem; font-weight: 600; }
.brand b { color: var(--muted); font-weight: 400; }
.repo-name { font-family: var(--font-mono); }
.github-mark { font-size: 30px; transition: transform .25s ease; }
.brand:hover .github-mark { transform: rotate(-8deg) scale(1.08); }
nav { display: flex; align-items: center; gap: clamp(18px, 3vw, 40px); margin-left: auto; }
nav a { position: relative; color: var(--muted); font-family: var(--font-mono); font-size: .78rem; font-weight: 600; }
nav a::after { content: ""; position: absolute; left: 0; bottom: -13px; width: 100%; height: 2px; background: var(--accent); transform: scaleX(0); transition: transform .25s ease; }
nav a:hover { color: var(--primary); }
nav a:hover::after { transform: scaleX(1); }
.header-actions { display: flex; align-items: center; gap: 8px; margin-left: 24px; order: 2; }
.theme-toggle, .menu-toggle { display: grid; place-items: center; width: 42px; height: 42px; color: var(--text); background: var(--surface-soft); border: 1px solid var(--border); border-radius: 50%; cursor: pointer; transition: transform .25s ease, background .25s ease; }
.theme-toggle:hover { color: var(--primary); transform: rotate(15deg) scale(1.05); }
.menu-toggle { display: none; gap: 4px; padding: 11px; }
.menu-toggle span { display: block; width: 19px; height: 2px; background: currentColor; transition: .3s ease; }
.menu-toggle.active span:nth-child(1) { transform: translateY(6px) rotate(45deg); }
.menu-toggle.active span:nth-child(2) { opacity: 0; }
.menu-toggle.active span:nth-child(3) { transform: translateY(-6px) rotate(-45deg); }
@media (max-width: 760px) {
  .site-header { min-height: 66px; padding: 8px 18px; }
  .repo-name { display: none; }
  .brand b { display: none; }
  .header-actions { margin-left: auto; }
  .menu-toggle { display: grid; }
  nav { position: absolute; top: calc(100% + 8px); left: 16px; right: 16px; display: grid; gap: 4px; padding: 12px; background: var(--surface); border: 1px solid var(--border); border-radius: 18px; box-shadow: var(--shadow); opacity: 0; visibility: hidden; transform: translateY(-12px); transition: .25s ease; }
  nav.active { opacity: 1; visibility: visible; transform: translateY(0); }
  nav a { padding: 12px 14px; border-radius: 10px; }
  nav a:hover { background: var(--surface-soft); }
  nav a::after { display: none; }
}

@media (max-width: 380px) {
  .site-header { padding-inline: var(--page-gutter); }
  .brand { font-size: .85rem; }
  .github-mark { font-size: 26px; }
  .header-actions { gap: 5px; }
  .theme-toggle, .menu-toggle { width: 38px; height: 38px; }
}
</style>
