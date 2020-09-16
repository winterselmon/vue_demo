<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="4"></v-col>
      <v-col cols="4">
        <v-img
          src="http://127.0.0.1:8887/new_logo.jpg"
          class="my"
          contain
          height="200"
        />
      </v-col>

      <v-col cols="4">
        <div class="b" style="margin-bottom:auto;margin-top:auto">
          <v-row class="text-center">
            <v-avatar>
              <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
            </v-avatar>
            <p class="login">Log in</p>
          </v-row>
        </div>
      </v-col>
    </v-row>

    <v-row style="margin-top:20px">
      <v-col></v-col>
      <v-col cols="2" md="1">
        <div class="my-2">
          <v-btn depressed large dark--black>HOME</v-btn>
        </div>
      </v-col>

      <v-col cols="2" md="1">
        <div class="my-2">
          <v-btn depressed large dark--black>MENU</v-btn>
        </div>
      </v-col>

      <v-col cols="2" md="1">
        <div class="my-2">
          <v-btn depressed large dark--black>ABOUT</v-btn>
        </div>
      </v-col>

      <v-col cols="2" md="1">
        <div class="my-2">
          <v-btn depressed large dark--black>CONTACT</v-btn>
        </div>
      </v-col>

      <v-col>
        <div class="round">
          <v-icon> </v-icon>
          <v-col v-for="value in ['l']" :key="value" cols="12" md="12">
            <div
              :class="`rounded-${value}-xl`"
              class="pa-7 text-center grey lighten-1"
              v-text="`Shop`"
            ></div>
          </v-col>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    valid: false,
    firstname: "",
    lastname: "",
    nameRules: [
      (v) => !!v || "Name is required",
      (v) => v.length <= 10 || "Name must be less than 10 characters",
    ],
    email: "",
    emailRules: [
      (v) => !!v || "E-mail is required",
      (v) => /.+@.+/.test(v) || "E-mail must be valid",
    ],
  }),
};
</script>

<!-- <v-col
        class="mb-5"
        cols="12"
      >
        <h2 class="headline font-weight-bold mb-3">
          What's next?
        </h2>

        <v-row justify="center">
          <a
            v-for="(next, i) in whatsNext"
            :key="i"
            :href="next.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ next.text }}
          </a>
        </v-row>
      </v-col>

      <v-col
        class="mb-5"
        cols="12"
      >
        <h2 class="headline font-weight-bold mb-3">
          Important Links
        </h2>

        <v-row justify="center">
          <a
            v-for="(link, i) in importantLinks"
            :key="i"
            :href="link.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ link.text }}
          </a>
        </v-row>
      </v-col>

      <v-col
        class="mb-5"
        cols="12"
      >
        <h2 class="headline font-weight-bold mb-3">
          Ecosystem
        </h2>

        <v-row justify="center">
          <a
            v-for="(eco, i) in ecosystem"
            :key="i"
            :href="eco.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ eco.text }}
          </a>
        </v-row>
      </v-col> -->

<script>
export default {
  name: "HelloWorld",

  data: () => ({
    ecosystem: [
      {
        text: "vuetify-loader",
        href: "https://github.com/vuetifyjs/vuetify-loader",
      },
      {
        text: "github",
        href: "https://github.com/vuetifyjs/vuetify",
      },
      {
        text: "awesome-vuetify",
        href: "https://github.com/vuetifyjs/awesome-vuetify",
      },
    ],
    importantLinks: [
      {
        text: "Documentation",
        href: "https://vuetifyjs.com",
      },
      {
        text: "Chat",
        href: "https://community.vuetifyjs.com",
      },
      {
        text: "Made with Vuetify",
        href: "https://madewithvuejs.com/vuetify",
      },
      {
        text: "Twitter",
        href: "https://twitter.com/vuetifyjs",
      },
      {
        text: "Articles",
        href: "https://medium.com/vuetify",
      },
    ],
    whatsNext: [
      {
        text: "Explore components",
        href: "https://vuetifyjs.com/components/api-explorer",
      },
      {
        text: "Select a layout",
        href: "https://vuetifyjs.com/getting-started/pre-made-layouts",
      },
      {
        text: "Frequently Asked Questions",
        href:
          "https://vuetifyjs.com/getting-started/frequently-asked-questions",
      },
    ],
  }),
};
</script>
<style>
div.b {
  position: absolute;
  right: 0;
  width: 10%;
  margin-right: 20px;
  margin-bottom: auto;
  margin-top: auto;
}

p.login {
  text-align: center;
  margin-left: 16px;
  margin-bottom: auto;
  margin-top: auto;
}

div.round {
  position: absolute;
  right: 0;
  width: 10%;
}
</style>
