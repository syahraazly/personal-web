<template>
  <section id="project" class="section">
    <div class="portfolio">
      <div class="text-skills">
        <h1>PORTFOLIO</h1>
        <p>Selected product and platform work.</p>
      </div>

      <div class="portfolio-update" role="status">
        <v-icon size="17">mdi-progress-pencil</v-icon>
        <span><b>Portfolio in progress</b> · I’m gradually adding more projects, context, and case-study details.</span>
        <small>last update · ongoing</small>
      </div>

      <div class="project-list">
        <article v-for="project in projects" :key="project.title" class="project-card">
          <div class="project-visual" :class="project.slug">
            <div class="project-visual-bar"><span>{{ project.imageLabel }}</span><span>{{ project.imageCount }} screens</span></div>
            <div v-if="project.slug === 'fitchick'" class="phone-showcase">
              <div class="phone phone-left"><img :src="project.previews[0]" alt="FitChick collection screen" /></div>
              <div class="phone phone-main"><img :src="project.cover" :alt="`${project.title} home screen`" /></div>
              <div class="phone phone-right"><img :src="project.previews[1]" alt="FitChick reward screen" /></div>
            </div>
            <img v-else :src="project.cover" :alt="`${project.title} preview`" />
          </div>
          <div class="project-content">
            <div class="project-meta"><span>{{ project.type }}</span><span>{{ project.period }}</span></div>
            <h2>{{ project.title }}</h2>
            <p class="project-role">{{ project.role }}</p>
            <p class="project-summary">{{ project.summary }}</p>
            <div class="project-details">
              <div><span>Contribution</span><p>{{ project.contribution }}</p></div>
              <div><span>Stack</span><ul><li v-for="item in project.stack" :key="item">{{ item }}</li></ul></div>
            </div>
            <div class="project-footer">
              <span :class="['project-status', project.access === 'Internal / NDA' ? 'private' : 'live']"><i></i>{{ project.access }}</span>
              <a v-if="project.link" :href="project.link" target="_blank" rel="noreferrer">Try on TestFlight <v-icon size="15">mdi-open-in-new</v-icon></a>
              <span v-else class="private-note"><v-icon size="15">mdi-lock-outline</v-icon> Screens use sanitized data</span>
            </div>
          </div>
        </article>
        <a class="github-link" href="https://github.com/syahraazly" target="_blank" rel="noreferrer"><v-icon size="16">mdi-github</v-icon> More experiments on GitHub <span>↗</span></a>
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
          <span>project-backed stack</span>
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
            <h3>Backend & integration</h3>
            <ul><li>PHP</li><li>Laravel</li><li>Spring Boot</li><li>REST API</li><li>API Integration</li></ul>
          </div>
          <div class="skill-group">
            <h3>Data & reporting</h3>
            <ul><li>MySQL</li><li>PostgreSQL</li><li>Oracle Database</li><li>Data Mapping</li><li>Operational Reporting</li></ul>
          </div>
          <div class="skill-group">
            <h3>iOS & product</h3>
            <ul><li>Swift</li><li>SwiftUI</li><li>HealthKit</li><li>TestFlight</li><li>Product Discovery</li></ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppProject",
  data() {
    return {
      projects: [
        {
          title: "Octomobile Portal", slug: "octomobile", type: "Banking operations portal", period: "2023 — 2025", role: "Frontend Developer · Backend support",
          summary: "An internal CIMB Niaga control center and approval portal for operational requests and customer-facing features in the Octomobile mobile banking application.",
          contribution: "Enhanced credit-card promotion management, built configuration for card offerings in the mobile app, and created reporting and history views to trace each card request through its workflow.",
          stack: ["Vue.js", "Spring Boot", "Oracle DB"], access: "Internal / NDA", imageLabel: "octomobile / promotion", imageCount: 1,
          cover: "/octomobile-promotion.png", previews: [], link: "",
        },
        {
          title: "SALMA", slug: "salma", type: "Logistics analytics platform", period: "2025 — present", role: "Fullstack Developer",
          summary: "Analysis System and Material Report is a web application for monitoring material stock and distribution across Telkom project operations, with real-time data and automated reporting for decision-making.",
          contribution: "Created new management menus and contributed across the product stack to make logistics data easier to monitor, analyze, and turn into operational reports.",
          stack: ["Vue.js", "Laravel", "REST API"], access: "Internal / NDA", imageLabel: "salma / home", imageCount: 1,
          cover: "/salma-home.png", previews: [], link: "",
        },
        {
          title: "iHLD", slug: "ihld", type: "Enterprise web platform", period: "2025 — present", role: "Fullstack Developer",
          summary: "An internal platform that supports planning and order workflows. The product continues to evolve through new menus, process improvements, and data-driven operational features.",
          contribution: "Built dashboards and new modules, reshaped order flows, mapped household data, integrated external APIs, and resolved ongoing production issues.",
          stack: ["Laravel", "MySQL", "PostgreSQL", "REST API"], access: "Internal / NDA", imageLabel: "ihld / dashboard", imageCount: 3,
          cover: "/ihld-dashboard.jpeg", previews: ["/ihld-order.jpeg", "/ihld-planning.jpeg"], link: "",
        },
        {
          title: "FitChick", slug: "fitchick", type: "iOS product", period: "2026", role: "iOS Developer · Rewards & HealthKit",
          summary: "A playful walking companion for people who are reluctant to walk but enjoy games. FitChick turns movement into a rewarding loop that gives users a reason to keep going farther.",
          contribution: "Managed the reward experience and HealthKit connection, helping translate walking activity into collectable progress and in-app motivation.",
          stack: ["Swift", "SwiftUI", "HealthKit", "TestFlight"], access: "Available on TestFlight", imageLabel: "fitchick / home", imageCount: 3,
          cover: "/fitchick-home.jpeg", previews: ["/fitchick-collect.jpeg", "/fitchick-reward.jpeg"], link: "https://testflight.apple.com/join/esSGgQVj",
        },
      ],
    };
  },
};
</script>

<style scoped>
.portfolio { padding-bottom: clamp(70px, 10vw, 120px); }
.text-skills { margin-bottom: 28px; }
.portfolio-update { display: flex; align-items: center; gap: 9px; margin: 0 0 20px; padding: 12px 16px; color: var(--muted); background: var(--surface-soft); border: 1px dashed var(--border); border-radius: 7px; font-family: var(--font-mono); font-size: .7rem; }.portfolio-update > .v-icon { flex: 0 0 auto; color: var(--accent); }.portfolio-update b { color: var(--text); font-weight: 600; }.portfolio-update small { margin-left: auto; white-space: nowrap; font-size: .64rem; }
.skill-file { overflow: hidden; background: var(--surface); border: 1px solid var(--border); border-radius: 8px; }
.file-bar {
  display: flex; justify-content: space-between; align-items: center; gap: 16px;
  padding: 11px 14px; color: var(--muted); background: var(--surface-soft);
  border-bottom: 1px solid var(--border); font-family: var(--font-mono); font-size: .76rem;
}
.file-bar span { display: flex; align-items: center; gap: 7px; }
.project-list { display: grid; gap: 20px; }.project-card { display: grid; grid-template-columns: minmax(320px, .92fr) minmax(0, 1.08fr); overflow: hidden; background: var(--surface); border: 1px solid var(--border); border-radius: 8px; transition: border-color .2s ease, box-shadow .2s ease; }.project-card:hover { border-color: var(--accent); box-shadow: var(--shadow); }.project-visual { position: relative; min-height: 390px; overflow: hidden; background: var(--code); border-right: 1px solid var(--border); }.project-visual-bar { position: absolute; z-index: 3; top: 0; right: 0; left: 0; display: flex; justify-content: space-between; padding: 10px 12px; color: var(--muted); background: color-mix(in srgb, var(--surface) 94%, transparent); border-bottom: 1px solid var(--border); font-family: var(--font-mono); font-size: .66rem; }.project-visual.ihld, .project-visual.salma, .project-visual.octomobile { display: flex; align-items: center; padding: 48px 18px 30px; background: linear-gradient(145deg, color-mix(in srgb, var(--accent) 8%, var(--surface-soft)), var(--code)); }.project-visual.ihld > img, .project-visual.salma > img, .project-visual.octomobile > img { width: 100%; height: auto; object-fit: contain; border: 1px solid var(--border); border-radius: 7px; box-shadow: 0 16px 34px rgba(0,0,0,.17); transition: transform .45s ease; }.project-card:hover .project-visual.ihld > img, .project-card:hover .project-visual.salma > img, .project-card:hover .project-visual.octomobile > img { transform: translateY(-4px); }.project-visual.fitchick { display: grid; place-items: end center; padding: 49px 14px 0; background: radial-gradient(circle at 50% 15%, color-mix(in srgb, var(--accent) 25%, transparent), transparent 46%), linear-gradient(145deg, var(--surface-soft), color-mix(in srgb, var(--accent) 10%, var(--surface-soft))); }.phone-showcase { position: relative; z-index: 1; display: flex; align-items: end; justify-content: center; width: 92%; height: 100%; }.phone { overflow: hidden; background: #111; border: 5px solid #111; border-bottom: 0; border-radius: 22px 22px 0 0; box-shadow: 0 14px 28px rgba(0,0,0,.24); }.phone img { display: block; width: 100%; height: 100%; object-fit: cover; object-position: top; }.phone-main { z-index: 2; width: 43%; aspect-ratio: 588 / 1280; max-height: 322px; }.phone-left, .phone-right { z-index: 1; width: 29%; aspect-ratio: 588 / 1280; max-height: 240px; margin-bottom: -20px; }.phone-left { margin-right: -9%; transform: rotate(-7deg); }.phone-right { margin-left: -9%; transform: rotate(7deg); }.project-card:hover .phone-main { transform: translateY(-7px); }.project-card:hover .phone-left { transform: rotate(-7deg) translateY(-4px); }.project-card:hover .phone-right { transform: rotate(7deg) translateY(-4px); }.phone, .phone-main, .phone-left, .phone-right { transition: transform .35s ease; }.project-content { display: flex; flex-direction: column; padding: clamp(24px, 4vw, 40px); }.project-meta { display: flex; justify-content: space-between; gap: 12px; color: var(--muted); font-family: var(--font-mono); font-size: .68rem; }.project-meta span:first-child { color: var(--accent); }.project-content h2 { margin: 16px 0 5px; font-size: clamp(1.65rem, 3vw, 2.35rem); letter-spacing: -.045em; }.project-role { color: var(--text); font-family: var(--font-mono); font-size: .76rem; }.project-summary { margin: 20px 0; color: var(--muted); font-size: .91rem; line-height: 1.7; }.project-details { display: grid; grid-template-columns: 1.1fr .9fr; gap: 22px; padding: 17px 0; border-top: 1px solid var(--border); }.project-details > div > span { color: var(--muted); font-family: var(--font-mono); font-size: .65rem; }.project-details p { margin-top: 7px; color: var(--text); font-size: .78rem; line-height: 1.6; }.project-details ul { display: flex; flex-wrap: wrap; gap: 5px; margin-top: 7px; padding: 0; list-style: none; }.project-details li { padding: 4px 6px; color: var(--text); background: var(--surface-soft); border: 1px solid var(--border); border-radius: 4px; font-family: var(--font-mono); font-size: .61rem; }.project-footer { display: flex; align-items: center; gap: 12px; margin-top: auto; padding-top: 16px; border-top: 1px solid var(--border); }.project-status, .private-note { display: inline-flex; align-items: center; gap: 6px; color: var(--muted); font-family: var(--font-mono); font-size: .65rem; }.project-status i { width: 7px; height: 7px; border-radius: 50%; background: var(--green); }.project-status.private i { background: var(--muted); }.project-footer a { display: inline-flex; align-items: center; gap: 5px; margin-left: auto; color: var(--accent); font-family: var(--font-mono); font-size: .7rem; }.project-footer a:hover { text-decoration: underline; }.github-link { display: flex; align-items: center; gap: 7px; width: fit-content; margin: 3px auto 0; color: var(--muted); font-family: var(--font-mono); font-size: .72rem; }.github-link:hover { color: var(--accent); }.github-link span { margin-left: 3px; }
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
  .portfolio-update { align-items: flex-start; line-height: 1.55; }.portfolio-update small { display: none; }
  .project-card { grid-template-columns: 1fr; }.project-visual { min-height: 290px; border-right: 0; border-bottom: 1px solid var(--border); }.project-visual.ihld, .project-visual.salma, .project-visual.octomobile { min-height: 300px; padding: 42px 14px 30px; }.project-visual.fitchick { padding-top: 46px; }.phone-showcase { width: 94%; }.phone-main { max-height: 255px; }.phone-left, .phone-right { max-height: 192px; }.project-content { padding: 24px 20px; }.project-details { grid-template-columns: 1fr; gap: 14px; }
  .skill-groups { grid-template-columns: 1fr; }
  .skill-group, .skill-group:nth-child(2n), .skill-group:nth-last-child(-n+2) { min-height: 0; border-right: 0; border-bottom: 1px solid var(--border); }
  .skill-group:last-child { border-bottom: 0; }
  .file-bar span:last-child { display: none; }
  .skill-group { padding: 24px 20px; }
}

@media (max-width: 390px) {
  .project-footer { align-items: flex-start; flex-direction: column; }.project-footer a { margin-left: 0; }
  .skill-group ul { gap: 8px 13px; }
}
</style>
