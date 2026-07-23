<template>
  <section id="contact" class="contact section">
      <h1>Ready to take your business to the next level?</h1>
      <p>Contact me today, and let’s discuss how I can help you achieve your goals!</p> <br>
      <v-btn variant="outlined" size="large" rounded href="mailto:syahraazly@gmail.com" target="_blank" style="text-decoration: none; text-transform: none;
              padding: 12px 24px; letter-spacing: 1px;">
        Let's get in touch
      </v-btn>
  </section>
</template>
<script>

export default {
  name: "AppContact",
};
</script>
<style>
.v-application__wrap {
  min-height: 0 !important;
}

.contact {
  position: relative;
  margin-bottom: clamp(40px, 8vw, 100px);
  padding: clamp(42px, 8vw, 90px);
  overflow: hidden;
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: clamp(24px, 4vw, 42px);
  box-shadow: var(--shadow);
}

.contact::after {
  content: "";
  position: absolute;
  right: -12%;
  bottom: -65%;
  width: 55%;
  aspect-ratio: 1;
  border-radius: 50%;
  background: var(--primary);
  opacity: .13;
  pointer-events: none;
}

.contact h1 {
  max-width: 900px;
  font-size: clamp(2.2rem, 6vw, 5rem);
  line-height: 1.05;
  font-weight: bold;
}

.contact p {
  max-width: 720px;
  margin-top: 22px;
  color: var(--muted);
  font-size: clamp(1rem, 2vw, 1.5rem);
}

/* untuk tablet */
@media (max-width: 1024px) {
  .contact { padding: clamp(36px, 7vw, 64px); }
}

/* untuk layar hp */
@media (max-width: 768px) {
  .contact { width: calc(100% - 28px); }
}

/* untuk layar kecil (hp kecil) */
@media (max-width: 480px) {
  .contact { padding: 32px 24px; }
}
</style>
