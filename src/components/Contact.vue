<template>
    <div class="contact-gradient">
        <v-container>
            <h1>Let's <span style="color: #EC5453">Work Together</span></h1>
            <v-row class="contact-text">
                <v-col cols="6">
                    <h2>Contact Information</h2><br>
                    <p>For inquiries, collaborations, or potential opportunities, kindly contact me using the information below:</p>
                    <br>
                    <div class="image-with-text">
                        <img src="gmail.png" alt="Gmail">
                        <span>syahraazly@gmail.com</span>
                    </div>
                    <div class="image-with-text">
                        <img src="linkedin.png" alt="LinkedIn">
                        <span>Syahra Zulya Shania Maghfiroh</span>
                    </div>
                    <div class="image-with-text">
                        <img src="github.png" alt="GitHub">
                        <span>syahraazly</span>
                    </div>
                </v-col>
                <v-col cols="6">
                    <v-form>
                        <div class="form-custom">
                            <v-text-field label="Name" variant="outlined"></v-text-field>
                            <v-row>
                                <v-col cols="6">
                                    <v-text-field label="Email" variant="outlined"></v-text-field>
                                </v-col>
                                <v-col cols="6">
                                    <v-text-field label="Phone Number" variant="outlined"></v-text-field>
                                </v-col>
                            </v-row>
                            <v-text-field label="Message" variant="outlined"></v-text-field>
                            <v-btn block size="x-large">Submit</v-btn>
                        </div>
                    </v-form>
                </v-col>
            </v-row>
        </v-container>
    </div>
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
.image-with-text {
    display: flex;
    align-items: center;
    margin-bottom: 1rem;
}
.image-with-text img {
    margin-right: 10px;
    width: 30px;
}
.form-custom {
    outline-color: #EC5453;
}
</style>