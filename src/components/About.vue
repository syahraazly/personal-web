<template>
    <v-app id="about">
        <div class="about">
            <div class="image-content"></div>
            <div class="text-content">
                <h2
                    style="color: #ec5453; font-weight: bold; font-size: 40px; text-align: center; margin-top: 2rem; margin-bottom: 2rem;">
                    About Me</h2>
                <p>Hi, my name is Syahra. I have a complex relationship with coding, which I sometimes like and
                    sometimes do not. However, for over 1 year, I've been exploring IT and focusing on Vue.js and
                    Laravel. Although I wasn't interested in the front end at first, over time, I decided to study and
                    pursue the field.</p>
                <br>
                <p>During this journey, I managed to develop a solid understanding of web development using Vue.js to
                    create dynamic and interactive user interfaces. I also have expertise in using Laravel as a powerful
                    back-end framework.</p>
                <br>
                <p>I really enjoy the challenge of completing projects involving this technology and am now increasingly
                    excited to continue improving my skills in the field of web development.</p>
            </div>
            <div class="image-content"></div>
        </div>
    </v-app>
</template>
<script>

export default {
    name: 'AppAbout'
}
</script>
<style>
.about {
    /* padding: 3rem; */
    background-color: #112032;
    color: #ffffff;
    display: flex;
    align-items: center;
    overflow: hidden;
}

.text-content {
    flex-basis: 50%;
    /* Menggunakan flex-basis daripada width untuk fleksibilitas dalam flexbox */
    padding: 3rem;
    background-color: #112032;
    color: #ffffff;
}

.image-content {
    flex-basis: 25%;
    /* Menetapkan basis fleksibel agar gambar tidak mengambil penuh 50% */
    height: 75vh;
    /* Menggunakan 100vh untuk memastikan gambar membentang penuh tinggi viewport */
    background-size: cover;
    background-repeat: no-repeat;
}

.image-content:first-child {
    background-image: url('../../public/syahra-right.png');
    background-position: left center;
    /* Menyelaraskan gambar ke kiri dan tengah secara vertikal */
}

.image-content:last-child {
    background-image: url('../../public/syahra-left.png');
    background-position: right center;
    /* Menyelaraskan gambar ke kanan dan tengah secara vertikal */
}


/* .about-photo {
    border-radius: 1rem;
    width: 100%;
    height: auto;

}

.about-text h1 {
    color: #EC5453;
} */
</style>