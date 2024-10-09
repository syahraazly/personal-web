<template>
    <v-app id="project">
        <div class="portfolio">
            <div class="text-skills">
                <h1>PORTFOLIO</h1>
                <p style="color: #6871d2">The <span style="color: #272727">Projects</span></p> <br>
            </div>
            <v-row>
                <v-col cols="12" md="4">
                    <v-card class="mx-auto" max-width="344">
                        <v-img src="Wikusama Hotels (1).png" height="200px" cover=""></v-img>
                        <v-card-title>
                            <h4 style="color: #6871d2">Wikusama Hotels</h4>
                        </v-card-title>
                        <v-card-text>The appearance of the Hotel Booking website uses the Laravel framework and
                            Vue.js.
                            <div class="card-text-custom">
                                <a href="https://github.com/syahraazly/hotel-vue">
                                    <span>View Code</span>
                                    <!-- <img src="panah.png" alt=""> -->
                                </a>
                            </div>
                        </v-card-text>
                    </v-card>
                </v-col>
                <v-col cols="12" md="4">
                    <v-card class="mx-auto" max-width="344">
                        <v-img src="Haji (1).png" height="200px" cover=""></v-img>
                        <v-card-title>
                            <h4 style="color: #6871d2">Landing Page Haji</h4>
                        </v-card-title>
                        <v-card-text>PERSADA website landing page displays using HTML/CSS and Javascript.
                            <div class="card-text-custom">
                                <a href="https://github.com/syahraazly/LP-Haji">
                                    <span>View Code</span>
                                    <!-- <img src="panah.png" alt=""> -->
                                </a>
                            </div>
                        </v-card-text>
                    </v-card>
                </v-col>
                <v-col cols="12" md="4">
                    <v-card class="mx-auto" max-width="344">
                        <v-img src="Start (1).png" height="200px" cover=""></v-img>
                        <v-card-title>
                            <h4 style="color: #6871d2">Recreate Start</h4>
                        </v-card-title>
                        <v-card-text>Recreate the START by @Joyshihab Landing Page design using HTML/CSS.
                            <div class="card-text-custom">
                                <a href="https://github.com/syahraazly/LP-START">
                                    <span>View Code</span>
                                    <!-- <img src="panah.png" alt=""> -->
                                </a>
                            </div>
                        </v-card-text>
                    </v-card>
                </v-col>
            </v-row>
            <div class="github">
                <a href="https://github.com/syahraazly" target="_blank">
                    <v-btn rounded prepend-icon="mdi-github" variant="outlined">
                        SEE MORE
                    </v-btn>
                </a>
            </div>
        </div>
        <div class="skills">
            <div class="text-skills">
                <h1>PROFESIONAL SKILL</h1>
                <p style="color: #6871d2">The <span style="color: #272727">Talents</span></p> <br>
            </div>
            <v-row class="skills">
                <v-col cols="4" md="2">
                    <v-btn variant="outlined">
                        HTML/CSS
                    </v-btn>
                </v-col><v-col cols="4" md="2">
                    <v-btn variant="outlined">
                        Javascript
                    </v-btn>
                </v-col>
                <v-col cols="4" md="2">
                    <v-btn variant="outlined">
                        PHP
                    </v-btn>
                </v-col>
                <v-col cols="4" md="2">
                    <v-btn variant="outlined">
                        Go
                    </v-btn>
                </v-col>
                <v-col cols="4" md="2">
                    <v-btn variant="outlined">
                        MYSQL
                    </v-btn>
                </v-col>
                <v-col cols="4" md="2">
                    <v-btn variant="outlined">
                        Laravel
                    </v-btn>
                </v-col><v-col cols="4" md="2">
                    <v-btn variant="outlined">
                        VueJS
                    </v-btn>
                </v-col>
                <v-col cols="4" md="2">
                    <v-btn variant="outlined">
                        NextJS
                    </v-btn>
                </v-col>
                <v-col cols="4" md="2">
                    <v-btn variant="outlined">
                        Quasar
                    </v-btn>
                </v-col>
                <v-col cols="4" md="2">
                    <v-btn variant="outlined">
                        Bootstrap
                    </v-btn>
                </v-col>
                <v-col cols="4" md="2">
                    <v-btn variant="outlined">
                        Vuetify
                    </v-btn>
                </v-col>
                <v-col cols="4" md="2">
                    <v-btn variant="outlined">
                        Saas
                    </v-btn>
                </v-col>
                <v-col cols="4" md="2">
                    <v-btn variant="outlined">
                        Git
                    </v-btn>
                </v-col><v-col cols="4" md="2">
                    <v-btn variant="outlined">
                        Postman
                    </v-btn>
                </v-col>
                <v-col cols="4" md="2">
                    <v-btn variant="outlined">
                        Office 365
                    </v-btn>
                </v-col>
            </v-row>
        </div>
    </v-app>
</template>
<script>

export default {
    name: 'AppProject'
}
</script>

<style>
.skills {
    padding-bottom: 6rem;
}

.experience {
    padding-bottom: 6rem;
}

.text-skills {
    font-weight: bold;
    text-align: center;
    margin-bottom: 2rem;
}

.text-skills h1 {
    font-size: 2rem;
}

.skills .v-btn {
    min-width: 120px;
    height: 50px;
    color: #272727;
    /* background-color: #6871d2; */
    margin: 5px;
}

.skills .v-btn:hover {
    background-image: linear-gradient(to left, #6871d2, #ffffff);
}

.portfolio {
    padding: 3rem;
}

.github {
    margin-top: 3rem;
    text-align: center;
}

.github a {
    text-decoration: none;
}

.github .v-btn:hover {
    background-image: linear-gradient(to left, #6871d2, #ffffff);
    color: #272727;
}

.card-text-custom {
    margin-top: 2rem;
}

.card-text-custom span {
    font-size: 15px;
}

.card-text-custom a {
    color: #6871d2;
    display: flex;
    text-decoration: none;
}

.card-text-custom img {
    margin-left: 1rem;
    width: 10px;
    height: 10px;
    display: flex;
}

.skills .v-btn:hover,
.techstacks .v-btn:hover {
    transition: background-color 0.3s ease, transform 0.3s ease;
}

.github a:hover {
    transition: color 0.3s ease;
    color: #6871d2;
}

.v-img {
    max-width: 100%;
    height: auto;
}

@media (max-width: 768px) {
    .experience {
        margin-top: 8rem;
    }

    .text-skills h1 {
        font-size: 1.5rem;
    }

    .experience h4,
    .experience-text h6 {
        font-size: 1rem;
    }

    .skills .v-btn,
    .techstacks .v-btn {
        min-width: 100px;
        font-size: x-small;
    }

    .experience-text {
        flex-direction: column;
        text-align: left;
    }

    .portfolio,
    .experience,
    .skills {
        padding: 2rem;
    }
}
</style>