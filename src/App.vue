<template>
  <div id="app">
    <v-app id="inspire">
      <Navbar class="App__nav" />
      <main class="App__main">
        <transition name="fade" type="out-in">
          <v-img
            height="100vh"
            gradient="to top, rgb(189,195,199,.75), rgba(44,62,80,.75)"
            src="https://images.pexels.com/photos/160107/pexels-photo-160107.jpeg"
          >
            <v-content id="content" class="fill-height" clipped-left>
              <v-container class="fill-height" fluid >
                <router-view></router-view>
              </v-container>
            </v-content>
          </v-img>
        </transition>
      </main>
      <v-footer color="rgba(0,0,0,0.02)" app inset>
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
  }
};
</script>
<style lang="scss">
.fade-enter-active,
.fade-leave-active {
  transition-duration: 0.3s;
  transition-property: opacity;
  transition-timing-function: ease;
}

.fade-enter,
.fade-leave-active {
  opacity: 0;
}
</style>