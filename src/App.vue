<template>
  <div id="app">
    <v-app id="portfolio">
      <Navbar class="App__nav" />
      <v-content clipped-left class="background-img">
        <transition name="fade" type="out-in">
          <router-view></router-view>
        </transition>
      </v-content>
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
$startColor: rgba(189, 195, 199, 0.75);
$endColor: rgba(44, 62, 80, 0.75);
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
.background-img {
  background-color: rgba(189, 195, 199, 0.75);
  background-image: url("https://images.pexels.com/photos/160107/pexels-photo-160107.jpeg");
  background-image: linear-gradient(
      to top rgba(189, 195, 199, 0.75),
      rgba(44, 62, 80, 0.75)
    ),
    url("https://images.pexels.com/photos/160107/pexels-photo-160107.jpeg");

  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
