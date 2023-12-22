<template>
  <v-app id="contact">
    <v-container>
      <div class="contact">
        <h1>CONTACT ME</h1>
        <p style="color: #6871d2">The <span style="color: #272727">Personal Info</span></p> <br>
      </div>
      <v-card>
        <v-form class="contact-form">
          <div class="form-custom">
            <v-text-field v-model="from_name" class="form-custom" label="Name" variant="outlined"></v-text-field>
            <v-text-field v-model="email" label="Email" variant="outlined"></v-text-field>
            <v-textarea v-model="message" label="Message" variant="outlined"></v-textarea>
            <v-btn tile color="#6871d2" block size="x-large" @click="sendEmail">Submit</v-btn>
          </div>
          <v-alert v-if="isEmailSent" color="#EC5453" theme="dark" icon="mdi-check" dense>
            Email Sent!
          </v-alert>
          <v-alert v-if="isEmailBounced" color="#2A3B4D" theme="dark" icon="mdi-alert" dense>
            Email Bounced!
          </v-alert>
          <v-alert v-if="isEmailRequired" color="#2A3B4D" theme="dark" icon="mdi-alert" dense>
            All field are required!
          </v-alert>
        </v-form>
      </v-card>
    </v-container>
  </v-app>
</template>
<script>
import emailjs from "@emailjs/browser";
import { createToast } from "mosha-vue-toastify";
import "mosha-vue-toastify/dist/style.css";

export default {
  name: "AppContact",
  data() {
    return {
      from_name: "",
      email: "",
      message: "",
    };
  },
  methods: {
    sendEmail() {
      if (this.from_name === "" || this.email === "" || this.message === "") {
        this.createAlert("All fields are required", "danger", 2000);
        return;
      }

      emailjs.send(
        "service_sy54zwlh5w",
        "template_fs57mrr",
        {
          from_name: this.from_name,
          email: this.email,
          message: this.message,
        },
        "DfVL9RR2ta3XaHSk0"
      )
        .then((response) => {
          console.log('SUCCESS!', response.status, response.text);
          this.createAlert("Email sent successfully", "success", 2000);
          this.from_name = "";
          this.email = "";
          this.message = "";
        }, (error) => {
          console.log('FAILED...', error);
          this.createAlert("Something went wrong", "danger", 5000);
        });
    },
    createAlert(message, type, timeout) {
      createToast(message, {
        position: "bottom-center",
        hideProgressBar: true,
        type: type,
        timeout: timeout,
        dismissible: true,
        pauseOnFocusLoss: true,
        pauseOnHover: true,
        closeOnClick: true,
        closeButton: true,
        icon: true,
        rtl: false,
      });
    },
  },
};
</script>
<style>
.contact {
  font-weight: bold;
  text-align: center;
  margin-bottom: 2rem;
}

.contact h1 {
  font-size: 2rem;
}

.contact-form {
  padding: 4rem;
}

.v-btn {
  transition: transform 0.3s ease;
}

.v-btn:hover {
  transform: scale(1.05);
}
</style>