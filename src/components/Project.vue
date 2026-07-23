<template>
    <section id="project" class="section">
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
                <h1>PROFESSIONAL SKILLS</h1>
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
                        Swift
                    </v-btn>
                </v-col>
                <v-col cols="4" md="2">
                    <v-btn variant="outlined">
                        SwiftUI
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
                        Tailwind CSS
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
                        Sass
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
    </section>
</template>
<script>

export default {
    name: 'AppProject'
}
</script>

<style>
.portfolio {
    padding-bottom: 6rem;
}

.skills {
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
    min-width: 100px;
    height: 50px;
    color: var(--text);
    background: var(--surface);
    border-color: var(--border);
    margin: 5px;
    box-shadow: 0 5px 15px transparent;
    transition: color .3s ease, background .3s ease, border-color .3s ease,
        box-shadow .3s ease, transform .3s cubic-bezier(.2, .8, .2, 1);
}

.skills .v-btn:hover {
    color: #ffffff;
    background: linear-gradient(135deg, var(--primary), var(--primary-soft));
    border-color: var(--primary);
    box-shadow: 0 12px 26px color-mix(in srgb, var(--primary) 35%, transparent);
    transform: translateY(-5px) scale(1.04);
}

.github {
    margin-top: 3rem;
    text-align: center;
}

.github a {
    text-decoration: none;
}

.github .v-btn:hover {
    color: #ffffff;
    background: var(--primary);
    border-color: var(--primary);
    box-shadow: 0 12px 28px color-mix(in srgb, var(--primary) 30%, transparent);
    transform: translateY(-4px);
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
    width: 10px;
    height: 10px;
    display: flex;
}

.github a:hover {
    color: var(--primary);
}

.v-img {
    max-width: 100%;
    height: auto;
}

@media (max-width: 768px) {
    .text-skills h1 {
        font-size: 1.5rem;
    }

    .skills .v-btn,
    .techstacks .v-btn {
        min-width: 80px;
        font-size: x-small;
    }
}
</style>
