<template>
  <v-img
    max-height="100vh"
    gradient="to top, rgb(189,195,199,.75), rgba(44,62,80,.75)"
    src="https://images.pexels.com/photos/160107/pexels-photo-160107.jpeg"
  >
    <v-content id="content" class="fill-height">
      <v-container class="fill-height" fluid clipped-left>
        <h1>This is an About page</h1>
      </v-container>
    </v-content>
  </v-img>
</template>

<script>
export default {
  name: "about"
}
</script>