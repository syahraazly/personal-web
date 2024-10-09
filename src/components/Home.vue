<template>
  <div class="home">
    <v-row>
      <v-col cols="12" md="6">
        <v-img src="..\..\public\syahraazly.png" contain max-height="400"></v-img>
      </v-col>
      <v-col cols="12" md="6">
        <div class="text">
          <h5>HELLO, <span style="color: #6871d2;">MY NAME IS</span></h5>
          <h1>SYAHRA <span style="color: #FEFEFE;">ZULYA</span></h1>
          <h6>I'am a <span>Frontend
              Developer</span></h6>
          <p>Based in East Java, Indonesia. Below are some of the projects I've worked on. <br> Thanks for stopping
            by!
            Read more about me here.</p>
          <div class="social">
            <a href="https://www.instagram.com/syahraazly" target="_blank">
              <i class='fab fa-instagram'></i>
            </a>
            <a href="https://www.linkedin.com/in/syahraazly" target="_blank">
              <i class='fab fa-linkedin'></i>
            </a>
          </div>
          <v-btn variant="outlined" class="download">
            <a href="/CV_Syahra Zulya Shania Maghfiroh.pdf" download>DOWNLOAD CV</a>
          </v-btn>
        </div>
      </v-col>
    </v-row>
  </div>
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
  background: #FEFEFE;
  padding-top: 12rem;
  padding-bottom: 6rem;
}

.text {
  color: #272727;
}

.text h5 {
  font-weight: bold;
}

.text h1 {
  font-weight: bold;
  font-size: 3rem;
  -webkit-text-stroke-width: 2px;
  -webkit-text-stroke-color: #272727;
  color: #6871d2;
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
  color: #272727;
  transition: color 0.3s ease;
  margin-top: 1rem;
  margin-bottom: 1rem;
  margin-right: 2rem;
}

.social i:hover {
  color: #6871d2;
}

.download {
  border-radius: 50px;
}

.download:hover {
  background-image: linear-gradient(to left, #6871d2, #ffffff);
  color: #272727;
  transition: background-color 0.3s ease, transform 0.3s ease;
}

/* .download a:hover {
  color: #6871d2;
} */

@media (max-width: 768px) {
  .text {
    padding: 2rem;
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
}
</style>