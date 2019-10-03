<template>
  <div id="app">
    <v-app id="inspire">
      <Navbar class="App__nav" />
      <main class="App__main">
        <transition name="fade" type="out-in">
          <router-view></router-view>
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