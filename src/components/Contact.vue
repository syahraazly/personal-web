<template>
  <section id="contact" class="contact section">
    <div class="text-skills contact-title">
      <h1>CONTACT</h1>
      <p>Start a conversation or explore a concise profile brief.</p>
    </div>

    <div class="contact-card">
      <div class="contact-copy">
        <span><b>Open</b> · available for a conversation</span>
        <h2>Ready to take your idea to the next level?</h2>
        <p>Tell me what you are working on, the problem you want to solve, or the role you think could be a good fit.</p>
      </div>
      <div class="contact-links">
        <a href="mailto:syahraazly@gmail.com"><v-icon size="18">mdi-email-outline</v-icon><span><small>Email</small>syahraazly@gmail.com</span></a>
        <a href="https://www.linkedin.com/in/syahraazly" target="_blank" rel="noreferrer"><v-icon size="18">mdi-linkedin</v-icon><span><small>LinkedIn</small>linkedin.com/in/syahraazly</span></a>
      </div>
    </div>

    <div class="assistant-heading">
      <p>syahraazly / personal-assist</p>
      <h1>A clearer picture, before you say hello.</h1>
      <span>A small public-profile assistant with the context that matters for a first conversation.</span>
    </div>

    <div class="assistant-workspace">
      <aside class="profile-brief" aria-label="Profile brief">
        <div class="brief-topline"><span><i></i> profile online</span><span>v1.0</span></div>
        <div class="person">
          <img src="/syahraazly.png" alt="Syahra Zulya" />
          <div><h2>Syahra Zulya</h2><p>@syahraazly · Jakarta, ID</p></div>
        </div>
        <p class="brief-intro">Software developer growing from frontend delivery into fullstack, product thinking, and iOS development.</p>

        <dl class="profile-facts">
          <div><dt>Current focus</dt><dd>Product discovery & iOS</dd></div>
          <div><dt>Core craft</dt><dd>Frontend & web systems</dd></div>
          <div><dt>Collaboration</dt><dd>Design, backend & product</dd></div>
        </dl>

        <div class="brief-section">
          <div class="brief-label"><span>Capabilities</span><small>selected</small></div>
          <div class="tag-list"><span v-for="skill in skills" :key="skill">{{ skill }}</span></div>
        </div>
        <div class="brief-section now-building">
          <div class="brief-label"><span>Currently building</span><small>now</small></div>
          <p>Human-centered product practice at Apple Developer Academy @ UC, Jakarta.</p>
        </div>
        <a class="brief-link" href="/CV_2024.pdf" download><v-icon size="16">mdi-download</v-icon> Download CV <span>↗</span></a>
      </aside>

      <div class="assistant-window">
        <div class="assistant-bar">
          <div><span class="online-dot"></span> personal-assist <em>public context only</em></div>
          <span>response time · instant</span>
        </div>

        <div ref="messages" class="messages" aria-live="polite">
          <div v-for="(message, index) in messages" :key="index" :class="['message', message.role]">
            <img v-if="message.role === 'assistant'" src="/syahraazly.png" alt="" />
            <div><b>{{ message.role === 'assistant' ? 'Syahra’s personal assist' : 'You' }}</b><p>{{ message.text }}</p></div>
          </div>
          <div v-if="isTyping" class="message assistant typing"><img src="/syahraazly.png" alt="" /><div><b>Syahra’s personal assist</b><p><i></i><i></i><i></i></p></div></div>
        </div>

        <div class="suggestions" aria-label="Suggested questions">
          <button v-for="suggestion in suggestions" :key="suggestion" type="button" :disabled="isTyping" @click="ask(suggestion)">{{ suggestion }}</button>
        </div>

        <form class="prompt-box" @submit.prevent="ask(input)">
          <span>&gt;</span>
          <input v-model="input" type="text" maxlength="180" autocomplete="off" placeholder="Ask about experience, strengths, or collaboration…" aria-label="Ask Syahra's profile assistant" />
          <button type="submit" :disabled="!input.trim() || isTyping" aria-label="Send question"><v-icon size="18">mdi-arrow-up</v-icon></button>
        </form>
        <p class="assistant-note"><v-icon size="13">mdi-shield-check-outline</v-icon> Limited to public profile notes. It does not access private data, inboxes, or live availability.</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppContact",
  data() {
    return {
      input: "", isTyping: false,
      skills: ["Vue.js", "Next.js", "JavaScript", "Laravel", "SwiftUI", "Product discovery"],
      messages: [{ role: "assistant", text: "Hi — I can give you a quick overview of Syahra’s experience, strengths, current learning, or how she likes to collaborate." }],
      suggestions: ["What is her experience?", "What is she learning now?", "How does she collaborate?", "What roles fit her?"],
    };
  },
  methods: {
    ask(question) {
      const cleanQuestion = question.trim();
      if (!cleanQuestion || this.isTyping) return;
      this.messages.push({ role: "user", text: cleanQuestion });
      this.input = ""; this.isTyping = true; this.scrollToLatest();
      window.setTimeout(() => {
        this.messages.push({ role: "assistant", text: this.getAnswer(cleanQuestion) });
        this.isTyping = false; this.scrollToLatest();
      }, 480);
    },
    getAnswer(question) {
      const value = question.toLowerCase();
      if (this.hasAny(value, ["academy", "akademi", "apple", "learning", "learn", "belajar", "ios", "swift", "product"])) return "She is currently learning product development and iOS at Apple Developer Academy @ UC, Jakarta. Her focus includes product discovery, user research, interface decisions, Swift, and SwiftUI — beginning with real user needs before shaping a solution.";
      if (this.hasAny(value, ["skill", "stack", "strength", "keahlian", "bisa apa", "technology", "teknologi"])) return "Her strongest working area is web frontend: JavaScript, Vue.js, Next.js, and Tailwind CSS. She also has experience with Laravel, REST APIs, MySQL, and is actively growing her Swift / SwiftUI practice. The combination is useful for product-minded web and iOS work.";
      if (this.hasAny(value, ["experience", "pengalaman", "company", "perusahaan", "work history", "career"])) return "Syahra has contributed to banking and enterprise web products at Telkomsigma and Infosys Solusi Terpadu, as well as Laravel web work and QA at Artcak Teknologi Indonesia. Her work has included UI improvements, feature modules, role access, API integration, data accuracy, and bug fixing.";
      if (this.hasAny(value, ["work", "kerja", "process", "proses", "team", "tim", "collaborat", "collaboration", "cara"])) return "Her approach is to clarify the problem and user needs first, then make progress in small, testable iterations. She is comfortable partnering with designers and backend developers, sharing context early, and translating feedback into practical implementation details.";
      if (this.hasAny(value, ["role", "opportunity", "position", "fit", "cocok", "hire", "hiring"])) return "She is open to conversations around Frontend, Fullstack, Business Analysis, and product-adjacent roles. A good fit is a team where she can combine technical delivery, collaboration, and thoughtful problem-solving while continuing to grow.";
      if (this.hasAny(value, ["contact", "email", "hubungi", "linkedin", "reach"])) return "The best way to start is by email at syahraazly@gmail.com or through LinkedIn. A short note about the role, project, or problem you are working on will make the conversation more useful.";
      if (this.hasAny(value, ["hello", "hi", "hai", "halo"])) return "Hello! Try asking about Syahra’s experience, current learning, core strengths, collaboration style, or the kinds of roles she is open to.";
      return "I only use a limited set of public profile notes. Try asking about Syahra’s experience, skills, current learning at the Academy, collaboration style, suitable roles, or contact details.";
    },
    hasAny(value, keywords) { return keywords.some((keyword) => value.includes(keyword)); },
    scrollToLatest() { this.$nextTick(() => { const container = this.$refs.messages; if (container) container.scrollTop = container.scrollHeight; }); },
  },
};
</script>

<style scoped>
.contact { padding-block: 0; }.contact > * { animation: none !important; opacity: 1 !important; }.contact-title { margin-bottom: 28px; }
.contact-card { display: grid; grid-template-columns: minmax(0, 1.35fr) minmax(280px, .65fr); gap: clamp(28px, 6vw, 72px); margin-bottom: clamp(70px, 10vw, 120px); padding: clamp(28px, 5vw, 52px); background: var(--surface); border: 1px solid var(--border); border-radius: 8px; }
.contact-copy > span { color: var(--muted); font-size: .82rem; }.contact-copy > span b { margin-right: 3px; padding: 4px 9px; color: #fff; background: var(--green); border-radius: 20px; font-family: var(--font-mono); font-size: .7rem; }.contact-copy h2 { max-width: 680px; margin: 20px 0 12px; font-size: clamp(1.7rem, 4vw, 3rem); line-height: 1.12; letter-spacing: -.04em; }.contact-copy p { max-width: 650px; color: var(--muted); font-size: 1rem; line-height: 1.75; }
.contact-links { display: flex; flex-direction: column; justify-content: center; gap: 10px; }.contact-links a { display: grid; grid-template-columns: 34px 1fr; align-items: center; gap: 8px; padding: 12px; color: var(--text); background: var(--surface-soft); border: 1px solid var(--border); border-radius: 7px; font-family: var(--font-mono); font-size: .76rem; transition: border-color .18s ease, transform .18s ease; }.contact-links a:hover { border-color: var(--accent); transform: translateX(3px); }.contact-links a > .v-icon { color: var(--accent); }.contact-links span { min-width: 0; overflow: hidden; text-overflow: ellipsis; white-space: nowrap; }.contact-links small { display: block; margin-bottom: 3px; color: var(--muted); font-size: .64rem; }
.assistant-heading { margin-bottom: 28px; }.assistant-heading > p { color: var(--muted); font-family: var(--font-mono); font-size: .78rem; }.assistant-heading h1 { margin: 8px 0 7px; font-size: clamp(2rem, 5vw, 3.7rem); line-height: 1.08; letter-spacing: -.045em; }.assistant-heading > span { color: var(--text); font-size: .92rem; }
.assistant-workspace { display: grid; grid-template-columns: minmax(255px, .7fr) minmax(0, 1.3fr); overflow: hidden; background: var(--surface); border: 1px solid var(--border); border-radius: 8px; box-shadow: var(--shadow); }.profile-brief { padding: 22px; background: var(--surface-soft); border-right: 1px solid var(--border); }.brief-topline, .brief-label { display: flex; justify-content: space-between; gap: 12px; color: var(--muted); font-family: var(--font-mono); font-size: .66rem; }.brief-topline span:first-child { color: var(--text); }.brief-topline i { display: inline-block; width: 7px; height: 7px; margin-right: 5px; border-radius: 50%; background: var(--green); }.person { display: flex; align-items: center; gap: 11px; margin: 23px 0 14px; }.person img { width: 46px; height: 46px; object-fit: cover; object-position: top; border: 1px solid var(--border); border-radius: 50%; }.person h2 { font-size: 1rem; letter-spacing: -.02em; }.person p { margin-top: 3px; color: var(--muted); font-family: var(--font-mono); font-size: .68rem; }.brief-intro { color: var(--muted); font-size: .86rem; line-height: 1.65; }.profile-facts { margin: 20px 0; border-top: 1px solid var(--border); }.profile-facts div { display: flex; justify-content: space-between; gap: 10px; padding: 9px 0; border-bottom: 1px solid var(--border); }.profile-facts dt { color: var(--muted); font-family: var(--font-mono); font-size: .65rem; }.profile-facts dd { text-align: right; font-size: .72rem; }.brief-section { margin-top: 20px; }.brief-label > span { color: var(--text); }.tag-list { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 10px; }.tag-list span { padding: 5px 7px; color: var(--text); background: var(--surface); border: 1px solid var(--border); border-radius: 4px; font-family: var(--font-mono); font-size: .65rem; }.now-building { padding: 12px; background: color-mix(in srgb, var(--accent) 6%, transparent); border: 1px solid color-mix(in srgb, var(--accent) 20%, var(--border)); border-radius: 6px; }.now-building p { margin-top: 8px; color: var(--muted); font-size: .76rem; line-height: 1.5; }.brief-link { display: flex; align-items: center; gap: 7px; margin-top: 18px; color: var(--text); font-family: var(--font-mono); font-size: .7rem; }.brief-link:hover { color: var(--accent); }.brief-link span { margin-left: auto; }
.assistant-window { min-width: 0; }.assistant-bar { display: flex; justify-content: space-between; align-items: center; gap: 14px; padding: 11px 15px; color: var(--muted); background: var(--surface-soft); border-bottom: 1px solid var(--border); font-family: var(--font-mono); font-size: .7rem; }.assistant-bar > div { display: flex; align-items: center; gap: 8px; color: var(--text); }.assistant-bar em { padding-left: 8px; color: var(--muted); border-left: 1px solid var(--border); font-style: normal; }.online-dot { width: 8px; height: 8px; border-radius: 50%; background: var(--green); box-shadow: 0 0 0 3px color-mix(in srgb, var(--green) 17%, transparent); }.messages { height: 360px; min-height: 280px; padding: clamp(18px, 4vw, 30px); overflow-y: auto; scroll-behavior: smooth; }.message { display: flex; width: fit-content; max-width: 94%; gap: 12px; margin-bottom: 20px; }.message.user { flex-direction: row-reverse; margin-left: auto; text-align: right; }.message img { width: 34px; height: 34px; flex: 0 0 auto; object-fit: cover; object-position: top; background: var(--surface-soft); border: 1px solid var(--border); border-radius: 50%; }.message > div { min-width: 0; }.message b { display: block; margin-bottom: 5px; color: var(--muted); font-family: var(--font-mono); font-size: .65rem; }.message.user b { text-align: right; }.message p { padding: 10px 13px; color: var(--text); background: var(--surface-soft); border: 1px solid var(--border); border-radius: 4px 12px 12px 12px; font-size: .9rem; font-weight: 500; line-height: 1.65; text-align: left; }.message.user p { color: #fff; background: var(--accent); border-color: var(--accent); border-radius: 12px 4px 12px 12px; }.typing p { display: flex; gap: 4px; padding-block: 15px; }.typing i { width: 5px; height: 5px; border-radius: 50%; background: var(--muted); animation: typing 1s infinite ease-in-out; }.typing i:nth-child(2) { animation-delay: .15s; }.typing i:nth-child(3) { animation-delay: .3s; }.suggestions { display: flex; flex-wrap: wrap; gap: 7px; padding: 0 clamp(18px, 4vw, 30px) 15px; }.suggestions button { padding: 6px 9px; color: var(--text); background: transparent; border: 1px solid var(--border); border-radius: 20px; font-size: .7rem; cursor: pointer; transition: color .18s ease, border-color .18s ease; }.suggestions button:hover:not(:disabled) { color: var(--accent); border-color: var(--accent); }.suggestions button:disabled { opacity: .55; cursor: wait; }.prompt-box { display: grid; grid-template-columns: auto 1fr auto; align-items: center; gap: 10px; margin: 0 clamp(18px, 4vw, 30px); padding: 8px 9px 8px 13px; background: var(--code); border: 1px solid var(--border); border-radius: 7px; }.prompt-box > span { color: var(--green); font-family: var(--font-mono); }.prompt-box input { width: 100%; min-width: 0; color: var(--text); background: transparent; border: 0; outline: 0; font-family: var(--font-mono); font-size: .78rem; }.prompt-box input::placeholder { color: var(--muted); }.prompt-box button { display: grid; place-items: center; width: 31px; height: 31px; color: #fff; background: var(--green); border: 0; border-radius: 6px; cursor: pointer; }.prompt-box button:disabled { cursor: not-allowed; opacity: .45; }.assistant-note { display: flex; align-items: flex-start; gap: 5px; padding: 10px clamp(18px, 4vw, 30px) 17px; color: var(--text); font-size: .65rem; line-height: 1.45; }.assistant-note .v-icon { flex: 0 0 auto; margin-top: 1px; }
@keyframes typing { 0%, 60%, 100% { transform: translateY(0); opacity: .45; } 30% { transform: translateY(-3px); opacity: 1; } }
@media (max-width: 820px) { .contact-card, .assistant-workspace { grid-template-columns: 1fr; }.profile-brief { border-right: 0; border-bottom: 1px solid var(--border); }.profile-facts { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; }.profile-facts div { display: block; }.profile-facts dd { margin-top: 5px; text-align: left; }.brief-section { display: inline-block; width: calc(50% - 10px); vertical-align: top; }.brief-section + .brief-section { margin-left: 16px; }.now-building { width: calc(50% - 10px); }.brief-link { margin-top: 16px; } }
@media (max-width: 600px) { .profile-brief { padding: 18px; }.brief-section, .now-building { display: block; width: auto; }.brief-section + .brief-section { margin-left: 0; }.profile-facts { grid-template-columns: 1fr; gap: 0; }.profile-facts div { display: flex; }.profile-facts dd { margin-top: 0; text-align: right; }.assistant-bar > span, .assistant-bar em { display: none; }.messages { height: 330px; padding-inline: 14px; }.message { max-width: 96%; }.message p { font-size: .84rem; }.suggestions { flex-wrap: nowrap; overflow-x: auto; padding-inline: 14px; }.suggestions button { flex: 0 0 auto; }.prompt-box { margin-inline: 14px; }.assistant-note { padding-inline: 14px; }.contact-card { padding: 24px 18px; }.contact-copy > span { display: flex; align-items: flex-start; flex-direction: column; gap: 9px; }.assistant-heading > span { display: block; line-height: 1.6; } }
</style>
