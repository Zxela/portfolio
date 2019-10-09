<template>
  <v-container class="fill-height" fluid>
    <v-row>
      <v-col v-for="(project, i) in projects" :key="i" cols="12" sm="6" md="4">
        <ProjectCard class="mx-auto" :project="project" />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import ProjectCard from "@/components/ProjectCard";

export default {
  name: "projects",
  components: { ProjectCard },
  data: () => ({
    projects: [
      {
        name: "Wallet Cryptorial",
        url: "https://github.com/Zxela/Wallet-Cryptorial",
        live: "",
        desc:
          "How-to on making a Cryptocurrency Wallet... Then make one for real and buy cryptocurrency from Coinbase via their buy API",
        blurb: "Cryptocurrency Wallet & Interactive Tutorial",
        img: "https://github.com/njlatcham/Wallet-Cryptorial/blob/master/docs/Home%20Page.png?raw=true"
      },
      {
        name: "Tweeter",
        url: "https://github.com/Zxela/tweeter",
        live: "",
        desc: "",
        blurb: "Tweeter is a simple, single-page Twitter clone.",
        img:
          "https://github.com/Zxela/tweeter/blob/master/docs/error.png?raw=true"
      },
      {
        name: "Chatty App",
        url: "https://github.com/Zxela/chatty-app",
        live: "",
        desc:
          "A simple messaging app written in JSX, Javascript, HTML and CSS; using WebSockets for real-time communication.",
        blurb: "Messaging app written in JSX using WebSockets",
        img:
          "https://github.com/Zxela/chatty-app/blob/master/docs/message.png?raw=true"
      },
      {
        name: "Tiny App",
        url: "https://github.com/Zxela/tinyapp",
        live: "",
        desc:
          "TinyApp is a full stack web application built with Node and Express that allows users to shorten long-URLs (à la bit.ly).",
        blurb: "Allows users to shorten long-URLs (à la bit.ly)",
        img:
          "https://github.com/Zxela/tinyapp/blob/master/docs/Screen%20Shot%202019-10-09%20at%2010.58.11%20AM.png?raw=true"
      },
      {
        name: "Jungle",
        url: "https://github.com/Zxela/jungle-rails",
        live: "",
        desc:
          "",
        blurb: "An e-commerce Rails app built for learning Rails",
        img:
          "https://github.com/Zxela/jungle-rails/blob/master/docs/home.png?raw=true"
      },
      {
        name: "Cryptocointalk.ca",
        url: "",
        live: "https://Cryptocointalk.ca",
        desc: "",
        blurb: "PHP/Wordpress News and Trading Platform",
        img: "https://github.com/Zxela/Cryptocointalk/blob/master/Screen%20Shot%202019-10-09%20at%2010.55.44%20AM.png?raw=true"
      }
    ]
  })
};
</script>