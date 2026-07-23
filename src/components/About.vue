<template>
    <section id="about" class="about section">
            <div class="image-content"></div>
            <div class="text-content">
                <h2
                    style="color: #ec5453; font-weight: bold; font-size: 40px; text-align: center; margin-top: 2rem; margin-bottom: 2rem;">
                    About Me</h2>
                <p>Hi, I'm Syahra, a software engineer transitioning from frontend to fullstack development. My
                    professional experience includes developing web applications with Next.js, Vue.js, and Tailwind
                    CSS for banking and enterprise projects.</p>
                <br>
                <p>I'm currently pursuing a degree in Information Systems while learning product development and iOS
                    development at the Apple Developer Academy @ UC, Jakarta. Through projects such as Cacta and
                    FitChick, I'm learning to begin with real user needs before turning ideas into products.</p>
                <br>
                <p>I'm open to opportunities in Business Analysis, Frontend, Fullstack, and other roles where I can
                    combine technical execution, collaboration, and problem-solving to create meaningful products.</p>
            </div>
            <div class="image-content"></div>
    </section>
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
