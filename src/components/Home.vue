<template>
  <div class="home">
    <v-container>
      <v-row class="home-text">
        <v-col cols="12" md="12">
          <v-img src="..\..\public\syahra.png" contain max-height="400"></v-img>
          <h2 style="color: #ec5453; font-weight: bold; font-size: 40px; text-align: center; margin-top: 2rem;">I am
            Syahra Zulya Shania Maghfiroh</h2>
          <h5 style="text-align: center; margin-top: 2rem;">Hi! I'am a <span style="font-weight: bold;">Front End Web
              Developer and Quality Assurance</span> based in East Java. <br> Below are some of the projects I've worked
            on. <br> Thanks for stopping by! Read more about me <a href="/CV_Syahra Zulya Shania Maghfiroh.pdf"
              download>here</a>.</h5>

          <!-- <h2>Hello, I'm</h2>
            <h1>
              Syahra Zulya<span style="color: #ec5453"> Shania Maghfiroh</span>
            </h1>
            <p class="mb-4">
              As a software engineering graduate, my ambition is to work in the
              IT field, specifically as a Web Developer and Quality Assurance.
              Open to work and quickly learn new technologies
            </p>
            <v-btn tile color="#EC5453" text @click="scroll('contact')"
              >hire me</v-btn
            > -->
        </v-col>
      </v-row>
    </v-container>
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
  /* background: linear-gradient(to right, #DFABBD, #79A0DC), linear-gradient(to bottom, rgba(255, 255, 255, 0), rgba(255, 255, 255, 1)); */
  background: #112032;
  padding-top: 8rem;
  padding-bottom: 3rem;
}

.home-text {
  color: #ffffff;
}

h5 a {
  font-size: inherit;
  /* Ini akan membuat teks dalam <a> mengikuti ukuran font dari <h5> */
  text-decoration: underline;
  /* Opsional: Menghilangkan garis bawah */
  /* Tambahkan gaya tambahan jika perlu */
}

/* .about-gradient {
  background: linear-gradient(to bottom, #9C96B8, #ffffff);
} */
.top {
  margin-top: 150px;
  /* margin-left: 50px; */
}

.top1 {
  margin-top: 80px;
}

.topInverse {
  margin-top: -250px;
}

.topTolbar {
  margin-top: 100px;
  text-align: center;
}

.first {
  width: 100%;
  height: 610px;
  /* background: linear-gradient(
    to right,#181818,#181818 50%, #111111 50%,#111111 50%
  ); */
  text-align: center;
  padding: 2rem 2rem;
}

.second {
  width: 100%;
  height: 400px;
  background: #181818;
  text-align: center;
  padding: 2rem 2rem;
}

.secondchild1 {
  display: inline-block;
  background-color: #1e1e1e;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: left;
  margin-top: 250px;
}

child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: left;
  margin-right: 8px;
}

.bgColor1 {
  background-color: #1e1e1e;
}

.bgColor2 {
  background-color: #ce1d2a;
}

.child1 {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  margin-right: 5px;
  width: 240px;
}

.child2 {
  display: inline-block;
  width: 245px;
  vertical-align: middle;
}

.mRight {
  margin-right: 8px;
}

.mButton {
  margin-bottom: 8px;
}

.padding {
  padding: 8px 0px;
}

.col-12.padd {
  padding: 12px 0 !important;
}

.col-12.childcol {
  padding: 0 !important;
}

h1.number {
  font-size: 50px;
  font-weight: bold;
}</style>