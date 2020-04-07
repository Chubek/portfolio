<template lang="pug">
div.main-div
    q-form(@submit="onSubmit" @reset="onReset")
        q-input(rounded filled v-model="name" type="text" label="Your Name")
        q-input(rounded filled v-model="subject" type="text" label="Your Business")
        q-input(rounded filled v-model="email" type="email" label="Your Email")
        q-input(rounded filled v-model="message" type="textarea" label="Your Message")
        div
            vue-recaptcha(:sitekey="siteKey")
                q-btn(label="Submit" type="submit" color="primary")
            q-btn(label="Reset" type="reset" color="primary")
      
        div.response
            {{ response }}

</template>
<script>
import nodemailer from "nodemailer";
import VueRecaptcha from "vue-recaptcha";
import "dotenv";
export default {
  name: "Contact",
  components: {
    VueRecaptcha,
  },
  data: () => ({
    name: null,
    subject: null,
    email: null,
    message: null,
    siteKey: process.env.RECAPTCHA_SITEKEY,
    gmailPassword: process.env.GMAIL_PASSWORD,
    response: null,
  }),
  methods: {
    onSubmit: function () {
      const transporter = nodemailer.createTransport({
        service: "gmail",
        auth: {
          user: "chubakbidpaa@gmail.com",
          pass: this.gmailPassword,
        },
      });
      const mailOptions = {
        from: "chubakbidpaa@gmail.com",
        to: "chubakbidpaa@gmail.com",
        subject: `[PORTFOLIO] from: ${this.name} regarding: ${this.subject}`,
        text: this.message,
      };

      transporter.sendMail(mailOptions, (error, info) => {
        if (error) {
          this.response = error;
        } else {
          this.response = "Email Sent!" + info.response;
        }
      });
    },
  },
};
</script>
