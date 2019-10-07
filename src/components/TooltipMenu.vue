<template>
  <v-row align="center" justify="space-around" class="mx-8 px-4">
    <v-tooltip bottom>
      <template v-slot:activator="{ on }">
        <v-btn href="https://github.com/zxela" target="_blank" icon large v-on="on">
          <v-icon v-if="$vuetify.breakpoint.mdAndUp" large>mdi-github-circle</v-icon>
          <v-icon v-else medium>mdi-github-circle</v-icon>
        </v-btn>
      </template>
      <span>My Github</span>
    </v-tooltip>

    <v-tooltip bottom>
      <template v-slot:activator="{ on }">
        <v-btn href="https://www.linkedin.com/in/alexzvaniga/" target="_blank" icon large v-on="on">
          <v-icon v-if="$vuetify.breakpoint.mdAndUp" large>mdi-linkedin-box</v-icon>
          <v-icon v-else medium>mdi-linkedin-box</v-icon>
        </v-btn>
      </template>
      <span>My LinkedIn</span>
    </v-tooltip>

    <v-tooltip bottom>
      <template v-slot:activator="{ on }">
        <v-btn
          href="https://resume.creddle.io/resume/2m8wwvhbtlk"
          icon
          large
          target="_blank"
          v-on="on"
        >
          <v-icon v-if="$vuetify.breakpoint.mdAndUp" large>mdi-file-account</v-icon>
          <v-icon v-else medium>mdi-file-account</v-icon>
        </v-btn>
      </template>
      <span>My Resume</span>
    </v-tooltip>

    <v-tooltip bottom>
      <template v-slot:activator="{ on }">
        <v-btn icon large @click="$router.push({name: 'contact'})" v-on="on">
          <v-icon v-if="$vuetify.breakpoint.mdAndUp" large>mdi-contact-mail</v-icon>
          <v-icon v-else medium>mdi-contact-mail</v-icon>
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