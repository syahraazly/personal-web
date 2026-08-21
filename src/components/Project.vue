<template>
  <section id="project" class="section">
    <div class="portfolio">
      <div class="text-skills">
        <h1>PORTFOLIO</h1>
        <p>Repositories and selected work.</p>
      </div>

      <div class="repo-shell">
        <div class="repo-toolbar">
          <span><v-icon size="16">mdi-source-branch</v-icon> main</span>
          <a href="https://github.com/syahraazly" target="_blank">
            <v-icon size="16">mdi-github</v-icon> View GitHub
          </a>
        </div>
        <div class="repo-empty">
          <v-icon size="30">mdi-archive-outline</v-icon>
          <h2>Work in progress</h2>
          <p>Project notes and case studies are being revised. I’ll publish them here when they are ready to read.</p>
          <span>Last updated: while cleaning up the docs</span>
        </div>
      </div>
    </div>

    <div class="skills">
      <div class="text-skills">
        <h1>PROFESSIONAL SKILLS</h1>
        <p>Tools I have used in real projects and ongoing practice.</p>
      </div>

      <div class="skill-file">
        <div class="file-bar">
          <span><v-icon size="16">mdi-file-document-outline</v-icon> stack.md</span>
          <span>18 tools</span>
        </div>
        <div class="skill-groups">
          <div class="skill-group">
            <h3>Frontend</h3>
            <ul>
              <li>HTML / CSS</li><li>JavaScript</li><li>Vue.js</li><li>Next.js</li>
              <li>Tailwind CSS</li><li>Quasar</li><li>Vuetify</li><li>Bootstrap</li>
            </ul>
          </div>
          <div class="skill-group">
            <h3>Backend & data</h3>
            <ul><li>PHP</li><li>Go</li><li>Laravel</li><li>MySQL</li></ul>
          </div>
          <div class="skill-group">
            <h3>Apple platforms</h3>
            <ul><li>Swift</li><li>SwiftUI</li></ul>
          </div>
          <div class="skill-group">
            <h3>Workflow</h3>
            <ul><li>Git</li><li>Postman</li><li>Sass</li><li>Office 365</li></ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default { name: "AppProject" };
</script>

<style scoped>
.portfolio { padding-bottom: clamp(70px, 10vw, 120px); }
.text-skills { margin-bottom: 28px; }
.repo-shell, .skill-file { overflow: hidden; background: var(--surface); border: 1px solid var(--border); border-radius: 8px; }
.repo-toolbar, .file-bar {
  display: flex; justify-content: space-between; align-items: center; gap: 16px;
  padding: 11px 14px; color: var(--muted); background: var(--surface-soft);
  border-bottom: 1px solid var(--border); font-family: var(--font-mono); font-size: .76rem;
}
.repo-toolbar span, .repo-toolbar a, .file-bar span { display: flex; align-items: center; gap: 7px; }
.repo-toolbar a { color: var(--text); }
.repo-toolbar a:hover { color: var(--accent); }
.repo-empty { padding: clamp(44px, 8vw, 84px) 24px; text-align: center; }
.repo-empty > .v-icon { margin-bottom: 15px; color: var(--muted); }
.repo-empty h2 { margin-bottom: 9px; font-size: clamp(1.3rem, 3vw, 1.75rem); letter-spacing: -.025em; }
.repo-empty p { max-width: 570px; margin: 0 auto 18px; color: var(--muted); font-size: .98rem; line-height: 1.7; }
.repo-empty span { color: var(--muted); font-family: var(--font-mono); font-size: .7rem; }
.skill-groups { display: grid; grid-template-columns: repeat(2, 1fr); }
.skill-group { min-height: 190px; padding: clamp(24px, 4vw, 38px); border-right: 1px solid var(--border); border-bottom: 1px solid var(--border); }
.skill-group:nth-child(2n) { border-right: 0; }
.skill-group:nth-last-child(-n+2) { border-bottom: 0; }
.skill-group h3 { margin-bottom: 18px; color: var(--text); font-family: var(--font-mono); font-size: .88rem; }
.skill-group h3::before { content: "## "; color: var(--muted); }
.skill-group ul { display: flex; flex-wrap: wrap; gap: 9px 18px; padding: 0; list-style: none; }
.skill-group li { position: relative; padding-left: 13px; color: var(--muted); font-size: .9rem; line-height: 1.6; transition: color .18s ease; }
.skill-group li::before { content: ""; position: absolute; top: .65em; left: 0; width: 5px; height: 5px; border-radius: 50%; background: var(--green); }
.skill-group li:hover { color: var(--text); }
@media (max-width: 700px) {
  .skill-groups { grid-template-columns: 1fr; }
  .skill-group, .skill-group:nth-child(2n), .skill-group:nth-last-child(-n+2) { min-height: 0; border-right: 0; border-bottom: 1px solid var(--border); }
  .skill-group:last-child { border-bottom: 0; }
  .file-bar span:last-child { display: none; }
  .repo-toolbar { align-items: flex-start; }
  .repo-toolbar a { flex: 0 0 auto; }
  .repo-empty { padding-inline: 18px; }
  .skill-group { padding: 24px 20px; }
}

@media (max-width: 390px) {
  .repo-toolbar { font-size: .68rem; }
  .repo-toolbar a { gap: 4px; }
  .skill-group ul { gap: 8px 13px; }
}
</style>
