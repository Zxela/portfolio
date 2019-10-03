<template>
  <v-row align="center" justify="space-around" class="mx-12 px-4">
    <v-tooltip bottom>
      <template v-slot:activator="{ on }">
        <v-btn href="https://github.com/zxela" target="_blank" icon large v-on="on">
          <v-icon large>mdi-github-circle</v-icon>
        </v-btn>
      </template>
      <span>My Github</span>
    </v-tooltip>

    <v-tooltip bottom>
      <template v-slot:activator="{ on }">
        <v-btn href="https://www.linkedin.com/in/alexzvaniga/" target="_blank" icon large v-on="on">
          <v-icon large>mdi-linkedin-box</v-icon>
        </v-btn>
      </template>
      <span>My LinkedIn</span>
    </v-tooltip>

    <v-tooltip bottom>
      <template v-slot:activator="{ on }">
        <v-btn :href="source" icon large target="_blank" v-on="on">
          <v-icon large>mdi-file-account</v-icon>
        </v-btn>
      </template>
      <span>My Resume</span>
    </v-tooltip>

    <v-tooltip bottom>
      <template v-slot:activator="{ on }">
        <v-btn
          icon
          large
          href="https://codepen.io/johnjleider/pen/bXNzZL"
          target="_blank"
          v-on="on"
        >
          <v-icon large>mdi-contact-mail</v-icon>
        </v-btn>
      </template>
      <span>Contact Me</span>
    </v-tooltip>
  </v-row>
</template>

<script>
export default {
  name: "Tooltip"
};
</script>

<style>
</style>