<template>
  <v-app id="contact">
    <div class="contact-gradient">
      <v-container>
        <h1 class="contact-tittle">
          Let's <span style="color: #ec5453">Work Together</span>
        </h1>
        <br />
        <v-row class="contact-text">
          <v-col cols="12" md="6">
            <h2>Contact Information</h2>
            <br />
            <p>
              For inquiries, collaborations, or potential opportunities, kindly
              contact me using the information below:
            </p>
            <br />
            <div class="image-with-text">
              <a href="mailto:syahraazly@gmail.com">
                <img src="gmail.png" alt="Gmail" />
                <span>syahraazly@gmail.com</span>
              </a>
            </div>
            <div class="image-with-text">
              <a
                href="https://www.linkedin.com/in/syahra-zulya-shania-maghfiroh-79a896223/"
              >
                <img src="linkedin.png" alt="LinkedIn" />
                <span>Syahra Zulya Shania Maghfiroh</span>
              </a>
            </div>
            <div class="image-with-text">
              <a href="https://github.com/syahraazly">
                <img src="github.png" alt="GitHub" />
                <span>syahraazly</span>
              </a>
            </div>
          </v-col>
          <v-col cols="12" md="6">
            <v-form>
              <div class="form-custom">
                <v-text-field
                  v-model="from_name"
                  class="form-custom"
                  label="Name"
                  variant="outlined"
                ></v-text-field>
                <v-text-field
                  v-model="email"
                  label="Email"
                  variant="outlined"
                ></v-text-field>
                <v-textarea
                  v-model="message"
                  label="Message"
                  variant="outlined"
                ></v-textarea>
                <v-btn
                  tile
                  color="#EC5453"
                  block
                  size="x-large"
                  @click="sendEmail"
                  >Submit</v-btn
                >
              </div>
              <v-alert
                v-if="isEmailSent"
                color="#EC5453"
                theme="dark"
                icon="mdi-check"
                dense
              >
                Email Sent!
              </v-alert>
              <v-alert
                v-if="isEmailBounced"
                color="#2A3B4D"
                theme="dark"
                icon="mdi-alert"
                dense
              >
                Email Bounced!
              </v-alert>
              <v-alert
                v-if="isEmailRequired"
                color="#2A3B4D"
                theme="dark"
                icon="mdi-alert"
                dense
              >
                All field are required!
              </v-alert>
            </v-form>
          </v-col>
        </v-row>
      </v-container>
    </div>
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
      try {
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
        );
        this.createAlert("Email sent successfully", "success", 2000);
      } catch (error) {
        this.createAlert("Something went wrong ${error}", "danger", 5000);
        console.log({ error });
      }

      // Reset form field
      this.from_name = "";
      this.email = "";
      this.message = "";
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
.contact-gradient {
  background: linear-gradient(to right, #dfabbd, #79a0dc),
    linear-gradient(to bottom, rgba(255, 255, 255, 0), rgba(255, 255, 255, 1));
  padding: 3rem;
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
.image-with-text a span {
    font-size: 20px;
}
.image-with-text img {
  margin-right: 10px;
  width: 30px;
  height: 25px;
}
.form-custom {
  outline-color: #ec5453;
}
</style>