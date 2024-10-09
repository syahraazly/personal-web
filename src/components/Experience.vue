<template>
    <v-app id="experience">
        <div class="experience">
            <div class="text-skills">
                <h1>EXPERIENCE</h1>
                <p style="color: #6871d2">The <span style="color: #272727">Journals</span></p> <br>
            </div>
            <v-row>
                <v-col cols="12" md="6">
                    <h4>Experience</h4>
                    <v-row>
                        <v-col cols="2">
                            <v-btn icon="$vuetify" variant="tonal" color="#6871d2">
                                <v-icon>mdi-briefcase-outline</v-icon>
                            </v-btn>
                        </v-col>
                        <v-col cols="10">
                            <h6 style="font-weight: bold;">PT. Infosys Solusi Terpadu</h6>
                            <div class="experience-text">
                                <h6 style="color: #6871d2; font-weight: 600;">Frontend Developer</h6>
                                <p>Jul 2023 - Present</p>
                            </div>
                            <p>Successfully created and improved various features on the web portal for CIMB Niaga
                                clients, improving functionality and overall user experience.</p>
                            <h6 style="font-weight: 600; margin-top: 1rem; margin-bottom: 1rem;">Related Techstacks
                            </h6>
                            <div class="techstacks">
                                <v-btn variant="outlined">
                                    Javascript
                                </v-btn>
                                <v-btn variant="outlined">
                                    Vuejs
                                </v-btn><v-btn variant="outlined">
                                    Quasar
                                </v-btn>
                            </div>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col cols="2">
                            <v-btn icon="$vuetify" variant="tonal" color="#6871d2">
                                <v-icon>mdi-briefcase-outline</v-icon>
                            </v-btn>
                        </v-col>
                        <v-col cols="10">
                            <h6 style="font-weight: bold;">PT. Artcak Teknologi Indonesia</h6>
                            <div class="experience-text">
                                <h6 style="color: #6871d2; font-weight: 600;">Fullstack Developer</h6>
                                <p>Aug 2022 - Nov 2022</p>
                            </div>
                            <p>Successfully managed and improved the web admin of Erpro, which is one of the
                                company's products, to improve its performance and efficiency.</p>
                            <div class="experience-text">
                                <h6 style="color: #6871d2; font-weight: 600;">Quality Assurance</h6>
                                <p>Jul 2022 - Aug 2022</p>
                            </div>
                            <p>Carry out the role as QA by finding and reporting bugs in company products, both for
                                web and mobile versions.</p>
                            <h6 style="font-weight: 600; margin-top: 1rem; margin-bottom: 1rem;">Related Techstacks
                            </h6>
                            <div class="techstacks">
                                <v-btn variant="outlined">
                                    HTML/CSS
                                </v-btn>
                                <v-btn variant="outlined">
                                    PHP
                                </v-btn><v-btn variant="outlined">
                                    Laravel
                                </v-btn><v-btn variant="outlined">
                                    Git
                                </v-btn><v-btn variant="outlined">
                                    Postman
                                </v-btn>
                            </div>
                        </v-col>
                    </v-row>
                </v-col>
                <v-col cols="12" md="6">
                    <h4>Education</h4>
                    <v-row>
                        <v-col cols="2">
                            <v-btn icon="$vuetify" variant="tonal" color="#6871d2">
                                <v-icon>mdi-school-outline</v-icon>
                            </v-btn>
                        </v-col>
                        <v-col cols="10">
                            <h6 style="font-weight: bold;">Universitas Terbuka</h6>
                            <div class="experience-text">
                                <h6 style="color: #6871d2; font-weight: 600;">Information Systems</h6>
                                <p>2023 - Present</p>
                            </div>
                            <p>Focus on studying business analysis and software development.</p>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col cols="2">
                            <v-btn icon="$vuetify" variant="tonal" color="#6871d2">
                                <v-icon>mdi-school-outline</v-icon>
                            </v-btn>
                        </v-col>
                        <v-col cols="10">
                            <h6 style="font-weight: bold;">SMK Telkom Malang</h6>
                            <div class="experience-text">
                                <h6 style="color: #6871d2; font-weight: 600;">Software Engineering</h6>
                                <p>2020 - 2023</p>
                            </div>
                            <p>Focus on learning the basics of programming, application development, and software
                                project management.</p>
                        </v-col>
                    </v-row>
                </v-col>
            </v-row>
        </div>
    </v-app>
</template>
<script>

export default {
    name: 'AppExperience'
}
</script>
<style>
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

.experience h4 {
    /* text-align: center; */
    font-weight: bold;
    margin-bottom: 2rem;
    font-size: 20px;
}

.experience-card {
    padding: 3rem;
    background-color: #6871d250;
}

.experience-text {
    display: flex;
    justify-content: space-between;
    text-align: justify;
    /* font-weight: bold; */
    margin-top: 1rem;
    width: 100%;
    /* Menentukan lebar untuk mengisi header */
}

.experience-text h6 {
    font-weight: bold;
    /* margin-right: 4rem; */
}

.techstacks .v-btn {
    margin-right: 5px;
    margin-bottom: 5px;
    font-size: small;
    /* color: #6871d2; */
}

.techstacks .v-btn:hover {
    background-image: linear-gradient(to left, #6871d2, #ffffff);
    color: #272727;
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