<template>
    <div class="about">
        <v-container>
            <v-row>
                <v-col cols="12" md="4">
                    <img class="about-photo" src="syahra (1).jpg" alt="">
                </v-col>
                <v-col cols="12" md="8" class="about-text">
                    <p>About</p>
                    <h1>About Me</h1>
                    <p>Hi, my name is Syahra. I have a complex relationship with coding, which I sometimes like and sometimes do not. However, for over 1 year, I've been exploring IT and focusing on Vue.js and Laravel. Although I wasn't interested in the front end at first, over time, I decided to study and pursue the field.</p>
                    <br>
                    <p>During this journey, I managed to develop a solid understanding of web development using Vue.js to create dynamic and interactive user interfaces. I also have expertise in using Laravel as a powerful back-end framework.</p>
                    <br>
                    <p>I really enjoy the challenge of completing projects involving this technology and am now increasingly excited to continue improving my skills in the field of web development.</p>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>
<script>

export default {
    name: 'AppAbout'
}
</script>
<style>
.about {
    padding: 3rem;
}
.about-photo {
    border-radius: 1rem;
    width: 100%;
    height: auto;
    
}
.about-text h1{
    color: #EC5453;
}
</style>