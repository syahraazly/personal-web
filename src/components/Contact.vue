<template>
  <v-app id="contact">
    <div class="contact">
      <h1>Ready to take your business to the next level?</h1>
      <p>Contact me today, and let’s discuss how I can help you achieve your goals!</p> <br>
      <v-btn variant="outlined" size="large" rounded href="mailto:syahraazly@gmail.com" target="_blank" style="text-decoration: none; text-transform: none;
              padding: 12px 24px; letter-spacing: 1px;">
        Let's get in touch
      </v-btn>
    </div>
  </v-app>
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
  padding: 0 1rem;
  margin-bottom: 10rem;
}

.contact h1 {
  font-size: 5rem;
  font-weight: bold;
}

.contact p {
  font-size: 2rem;
}

/* untuk tablet */
@media (max-width: 1024px) {
  .contact h1 {
    font-size: 3rem;
  }

  .contact p {
    font-size: 1.5rem;
  }
}

/* untuk layar hp */
@media (max-width: 768px) {
  .contact h1 {
    font-size: 2.5rem;
  }

  .contact p {
    font-size: 1.2rem;
  }
}

/* untuk layar kecil (hp kecil) */
@media (max-width: 480px) {
  .contact h1 {
    font-size: 2rem;
  }

  .contact p {
    font-size: 1rem;
  }
}
</style>