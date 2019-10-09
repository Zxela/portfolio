<template>
  <v-card color="grey lighten-3" class="elevation-10" max-width="344">
    <v-img :src="project.img" height="200px" class="elevation-2"></v-img>
    <v-divider />
    <v-card-title>
      <div>{{project.name}}</div>
      <span class="grey--text subtitle-2">{{project.blurb}}</span>
    </v-card-title>

    <v-card-actions>
      <v-btn v-if="project.url" @click="click(project.url)" text>Repo</v-btn>

      <v-btn v-if="project.live" @click="click(project.live)" text color="purple">Live</v-btn>

      <div class="flex-grow-1"></div>

      <v-btn v-if="project.desc" icon @click="show = !show">
        <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-card-text>{{project.desc}}</v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
export default {
  name: "Project Card",
  props: ["project"],
  data: () => ({
    show: false
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

<style>
</style>