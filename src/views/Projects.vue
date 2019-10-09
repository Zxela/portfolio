<template>
  <v-container class="fill-height" fluid>
    <v-row>
      <v-col v-for="(project, i) in projects" :key="i" cols="12" sm="6" md="4">
        <v-card height="300px" color="rgba(250,250,250,0.8)">
          <v-card-title>
            <v-col>
              <v-row justify="center">{{project.name}}</v-row>
              <v-row>
                <v-divider />
              </v-row>
            </v-col>
          </v-card-title>
          <v-col>
            <v-card-text>{{project.desc}}</v-card-text>
          </v-col>
          <v-col>
            <v-card-actions>
              <v-btn @click="click(project.url)">Check it out</v-btn>
            </v-card-actions>
          </v-col>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "projects",
  data: () => ({
    projects: [
      {
        name: "Wallet Cryptorial",
        url: "https://github.com/Zxela/Wallet-Cryptorial",
        desc:
          "How-to on making a Cryptocurrency Wallet... Then make one for real and buy cryptocurrency from Coinbase via their buy API",
        img: ""
      },
      {
        name: "Tweeter",
        url: "https://github.com/Zxela/tweeter",
        desc: "Tweeter is a simple, single-page Twitter clone.",
        img: ""
      },
      {
        name: "Chatty App",
        url: "https://github.com/Zxela/chatty-app",
        desc:
          "A simple messaging app written in JSX, Javascript, HTML and CSS; using WebSockets for real-time communication.",
        img: "https://github.com/Zxela/chatty-app/blob/master/docs/message.png"
      },
      {
        name: "Tiny App",
        url: "https://github.com/Zxela/tinyapp",
        desc:
          "TinyApp is a full stack web application built with Node and Express that allows users to shorten long-URLs (à la bit.ly).",
        img:
          "https://raw.githubusercontent.com/Zxela/tinyapp/master/docs/listTinyApp.png"
      },
      {
        name: "Jungle",
        url: "https://github.com/Zxela/jungle-rails",
        desc:
          "An e-commerce Rails app built for learning Rails through example",
        img:
          "https://github.com/Zxela/jungle-rails/blob/master/docs/home.png?raw=true"
      },
      {
        name: "Cryptocointalk.ca",
        url: "Cryptocointalk.ca",
        desc: "PHP/Wordpress News and Trading Platform",
        img: "https://github.com/Zxela/tweeter/blob/master/docs/error.png"
      }
    ]
  }),
  methods: {
    click(url) {
      if (url) {
        window.location = url;
      } else {
        return;
      }
    }
  }
};
</script>