<template>
    <v-app id="experience">
        <div class="skills-bg">
            <v-container>
                <p>My Skills</p>
                <h1 style="color: #EC5453">My Expertise</h1> <br>
                <v-row>
                    <v-col cols="6" md="3">
                        <v-card class="mx-auto">
                            <v-card class="skills-logo">
                                <img src="code (1).png" alt="">
                            </v-card>
                            <v-card-title>
                                Web Development
                            </v-card-title>
                            <v-card-text>
                                Understanding of programming languages, and UI plugins.
                            </v-card-text>
                        </v-card>
                    </v-col>
                    <v-col cols="6" md="3">
                        <v-card class="mx-auto">
                            <v-card class="skills-logo">
                                <img src="wireframe (1).png" alt="">
                            </v-card>
                            <v-card-title>
                                Web Design
                            </v-card-title>
                            <v-card-text>
                                Responsive design understanding and familiarity with Figma.
                            </v-card-text>
                        </v-card>
                    </v-col>
                    <v-col cols="6" md="3">
                        <v-card class="mx-auto">
                            <v-card class="skills-logo">
                                <img src="briefcase (1).png" alt="">
                            </v-card>
                            <v-card-title>
                                Creative Work
                            </v-card-title>
                            <v-card-text>
                                Design an attractive and responsive website look and layout.
                            </v-card-text>
                        </v-card>
                    </v-col>
                    <v-col cols="6" md="3">
                        <v-card class="mx-auto">
                            <v-card class="skills-logo">
                                <img src="settings.png" alt="">
                            </v-card>
                            <v-card-title>
                                Quality Control
                            </v-card-title>
                            <v-card-text>
                                Skilled and meticulous in performing software testing.
                            </v-card-text>
                        </v-card>
                    </v-col>
                </v-row>
                
            </v-container>
        </div>
        <div class="portfolio">
            <v-container>
                <p class="project">Recent Project</p>
                <v-row>
                    <v-col cols="12" md="10">
                        <h1 style="color: #EC5453">My Portfolio</h1>
                    </v-col>
                    <v-col cols="12" md="2">
                        <div class="github">
                            <a href="https://github.com/syahraazly" target="_blank">
                                <v-btn class="text-none" color="#EC5453" prepend-icon="mdi-github" style="font-size: 10px">
                                    View My Github
                                </v-btn>
                            </a>
                        </div>
                    </v-col>
                </v-row>
                <v-row>
                    <v-col cols="12" md="4">
                        <v-card class="mx-auto" max-width="344">
                            <v-img src="Wikusama Hotels (1).png" height="200px" cover=""></v-img>
                            <v-card-title><h4 style="color: #EC5453">Wikusama Hotels</h4></v-card-title>
                            <v-card-text>The appearance of the Hotel Booking website uses the Laravel framework and Vue.js.
                                <div class="card-text-custom">
                                <a href="https://github.com/syahraazly/hotel-vue">
                                    <span>View Code</span>
                                    <img src="panah.png" alt="">
                                </a>
                                </div>
                            </v-card-text>
                        </v-card>
                    </v-col>
                    <v-col cols="12" md="4">
                        <v-card class="mx-auto" max-width="344">
                            <v-img src="Haji (1).png" height="200px" cover=""></v-img>
                            <v-card-title><h4 style="color: #EC5453">Landing Page Haji</h4></v-card-title>
                            <v-card-text>PERSADA website landing page displays using HTML/CSS and Javascript.
                                <div class="card-text-custom">
                                <a href="https://github.com/syahraazly/LP-Haji">
                                    <span>View Code</span>
                                    <img src="panah.png" alt="">
                                </a>
                                </div>
                            </v-card-text>
                        </v-card>
                    </v-col>
                    <v-col cols="12" md="4">
                        <v-card class="mx-auto" max-width="344">
                            <v-img src="Start (1).png" height="200px" cover=""></v-img>
                            <v-card-title><h4 style="color: #EC5453">Recreate Start</h4></v-card-title>
                            <v-card-text>Recreate the START by @Joyshihab Landing Page design using HTML/CSS.
                                <div class="card-text-custom">
                                <a href="https://github.com/syahraazly/LP-START">
                                    <span>View Code</span>
                                    <img src="panah.png" alt="">
                                </a>
                                </div>
                            </v-card-text>
                        </v-card>
                    </v-col>
                </v-row>
            </v-container>
        </div>
    </v-app>
</template>
<script>

export default{
    name: 'AppExperience'
}
</script>
<style>
.skills-bg {
    background: #E0D7E2;
    padding: 3rem;
}
.card-custom {
    color: black;
    background-color: #BCD0EE;
    text-align: center;
}
.skills-logo {
    margin: 1rem;
    padding: 5px;
    display: flex;
    width: 30px;
    height: 30px;
    background-color: #bcd0ee6a;
}
.portfolio {
    padding: 3rem;
}
.github a{
    text-decoration: none;
    color: #ffffff;
}
.card-text-custom {
    margin-top: 2rem;
}
.card-text-custom span {
    font-size: 15px;
}
.card-text-custom a {
    color: #EC5453;
    display: flex;
    text-decoration: none;
}
.card-text-custom img {
    margin-left: 1rem;
    width: 10px;
    height: 10px;
    display: flex;
}
</style>