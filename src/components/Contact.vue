<template>
<v-app id="contact">
    <div class="contact-gradient">
        <v-container>
            <h1 class="contact-tittle">Let's <span style="color: #EC5453">Work Together</span></h1> <br>
            <v-row class="contact-text">
                <v-col cols="12" md="6">
                    <h2>Contact Information</h2><br>
                    <p>For inquiries, collaborations, or potential opportunities, kindly contact me using the information below:</p>
                    <br>
                    <div class="image-with-text">
                        <a href="mailto:syahraazly@gmail.com">
                            <img src="gmail.png" alt="Gmail">
                            <span>syahraazly@gmail.com</span>
                        </a>
                    </div>
                    <div class="image-with-text">
                        <a href="https://www.linkedin.com/in/syahra-zulya-shania-maghfiroh-79a896223/">
                            <img src="linkedin.png" alt="LinkedIn">
                            <span>Syahra Zulya Shania Maghfiroh</span>
                        </a>
                    </div>
                    <div class="image-with-text">
                        <a href="https://github.com/syahraazly">
                            <img src="github.png" alt="GitHub">
                            <span>syahraazly</span>
                        </a>
                    </div>
                </v-col>
                <v-col cols="12" md="6">
                    <v-form>
                        <div class="form-custom">
                            <v-text-field class="form-custom" label="Name" variant="outlined"></v-text-field>
                            <v-row>
                                <v-col cols="12" md="6">
                                    <v-text-field label="Email" variant="outlined"></v-text-field>
                                </v-col>
                                <v-col cols="12" md="6">
                                    <v-text-field label="Phone Number" variant="outlined"></v-text-field>
                                </v-col>
                            </v-row>
                            <v-textarea label="Message" variant="outlined"></v-textarea>
                            <v-btn tile color="#EC5453" block size="x-large">Submit</v-btn>
                        </div>
                    </v-form>
                </v-col>
            </v-row>
        </v-container>
    </div>
</v-app>
</template>
<script>

export default{
    name : 'AppContact'

}
</script>
<style>
.contact-gradient {
  background: linear-gradient(to right, #DFABBD, #79A0DC), linear-gradient(to bottom, rgba(255, 255, 255, 0), rgba(255, 255, 255, 1));
}
.contact-text {
    color: #ffffff;
}
.contact-tittle {
    text-align: center;
    font-size: 3rem;
    color: #ffffff;
}
.image-with-text {
    display: flex;
    align-items: center;
    margin-bottom: 1rem;
}
.image-with-text a {
    display: flex;
    text-decoration: none;
    color: inherit;
}
.image-with-text img {
    margin-right: 10px;
    width: 30px;
}
.form-custom {
    outline-color: #EC5453;
}
</style>