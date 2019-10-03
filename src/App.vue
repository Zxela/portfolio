<template>
  <div id="app">
    <v-app id="portfolio">
      <!-- Navigation -->
      <Navbar />
      <!-- Site Content -->
      <v-content>
        <!-- Container fills  -->
        <v-container class="fill-height" fluid>
          <v-col>
            <v-row align="center" justify="center"></v-row>
            <v-divider />
            
          </v-col>
        </v-container>
      </v-content>

      <v-footer app>
        <span>&copy; 2019 Alex Zvaniga</span>
      </v-footer>
    </v-app>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar";

export default {
  components: { Navbar },
  props: {
    source: String
  },
  created() {
    this.$vuetify.theme.dark = true;
  }
};
</script>
<style lang="scss">
</style>