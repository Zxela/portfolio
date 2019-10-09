<template>
  <v-row align="center" justify="space-around" class="mx-6 px-4">
    <v-tooltip bottom>
      <template v-slot:activator="{ on }">
        <v-btn icon large @click="$router.push({name: 'projects'})" v-on="on">
          <v-icon v-if="$vuetify.breakpoint.mdAndUp" large>mdi-view-dashboard</v-icon>
          <v-icon v-else medium>mdi-view-dashboard</v-icon>
        </v-btn>
      </template>
      <span>My Portfolio</span>
    </v-tooltip>

    <v-tooltip bottom>
      <template v-slot:activator="{ on }">
        <v-btn icon large @click="$router.push({name: 'about'})" v-on="on">
          <v-icon v-if="$vuetify.breakpoint.mdAndUp" large>mdi-account-tie</v-icon>
          <v-icon v-else medium>mdi-account-tie</v-icon>
        </v-btn>
      </template>
      <span>About Me</span>
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

    <v-tooltip bottom>
      <template v-slot:activator="{ on }">
        <v-btn href="https://github.com/zxela" target="_blank" icon large v-on="on">
          <v-icon v-if="$vuetify.breakpoint.mdAndUp" large>mdi-github-circle</v-icon>
          <v-icon v-else medium>mdi-github-circle</v-icon>
        </v-btn>
      </template>
      <span>My Github</span>
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