<template>
  <div id="app">
    <v-app id="inspire">
      <Navbar />
      <router-view></router-view>
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
    this.$vuetify.theme.dark = false;
  }
};
</script>
<style lang="scss">
</style>