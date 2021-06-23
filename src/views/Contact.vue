<template>
  <v-main>
    <div class="staticHero">
      <v-img
        max-height="275px"
        src="https://luantravelperu.com/wp-content/uploads/2018/04/reach_us.png"
        gradient="to top right, rgba(0,0,0,.3), rgba(0,0,0,.2)"
      >
        <v-row align="end" class="ligthbox white--text pa-2 fill-height">
          <v-col>
            <v-container>
              <div class="headline">Contact us</div>
            </v-container>
          </v-col>
        </v-row>
      </v-img>
    </div>
    <v-container>
      <v-form ref="form" @submit.prevent="sendEmail" id="myForm">
        <v-text-field
          type="text"
          v-model="name"
          :counter="40"
          :rules="nameRules"
          label="Name"
          required
        ></v-text-field>
        <v-text-field
          type="email"
          v-model="email"
          :rules="emailRules"
          label="E-mail"
          required
        ></v-text-field>
        <v-textarea
          name="message"
          v-model="message"
          cols="30"
          rows="5"
          placeholder="Message"
          required
        >
        </v-textarea>

        <v-btn
          type="submit"
          :disabled="!valid"
          color="#343A40"
          class="mr-4 white--text"
        >
          Submit
        </v-btn>
      </v-form>
    </v-container>
  </v-main>
</template>
<script>
import emailjs from "emailjs-com";
export default {
  name: "ContactUs",
  data: () => ({
    valid: true,
    name: "",
    nameRules: [
      (v) => !!v || "Name is required",
      (v) => (v && v.length <= 40) || "Name must be less than 40 characters",
    ],
    email: "",
    emailRules: [
      (v) => !!v || "E-mail is required",
      (v) => /.+@.+\..+/.test(v) || "E-mail must be valid",
    ],
    message: "",
    messageRules: [
      (v) => !!v || "Message is required",
      (v) => (v && v.length >= 10) || "Message must be more than 10 characters",
    ],
  }),
  methods: {
    sendEmail(e) {
      try {
        emailjs.sendForm("c2rp3rntry_3q1jfqf", "template_ph0bqm4", "#myForm", "user_JV1afxxDDX9rbg3IOlE7i").then(
          function (response) {
            console.log("SUCCESS!", response.status, response.text);
          },
          function (error) {
            console.log("FAILED...", error);
          }
        );
      } catch (error) {
        console.log({ error });
      }
      // Reset form field
      this.name = "";
      this.email = "";
      this.message = "";
    },
  },
};
</script>
