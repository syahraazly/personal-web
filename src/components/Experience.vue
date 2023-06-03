<template>
    <v-app id="experience">
        <div class="skills-bg">
            <v-container>
                <p>My Skills</p>
                <h1 style="color: #EC5453">My Expertise</h1> <br>
                <v-row>
                    <v-col cols="6" md="3">
                        <v-card text="HTML" variant="tonal" class="card-custom"></v-card>
                    </v-col>
                    <v-col cols="6" md="3">
                        <v-card text="CSS" variant="tonal" class="card-custom"></v-card>
                    </v-col>
                    <v-col cols="6" md="3">
                        <v-card text="PHP" variant="tonal" class="card-custom"></v-card>
                    </v-col>
                    <v-col cols="6" md="3">
                        <v-card text="SQL Database" variant="tonal" class="card-custom"></v-card>
                    </v-col>
                </v-row>
                <v-row>
                    <v-col cols="6" md="3">
                        <v-card text="Vue" variant="tonal" class="card-custom"></v-card>
                    </v-col>
                    <v-col cols="6" md="3">
                        <v-card text="Vuetify" variant="tonal" class="card-custom"></v-card>
                    </v-col>
                    <v-col cols="6" md="3">
                        <v-card text="Laravel" variant="tonal" class="card-custom"></v-card>
                    </v-col>
                    <v-col cols="6" md="3">
                        <v-card text="Git" variant="tonal" class="card-custom"></v-card>
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
}
.card-custom {
    color: black;
    background-color: #BCD0EE;
    text-align: center;
}
</style>