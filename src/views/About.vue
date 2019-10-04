<template>
  <v-container class="fill-height justify-center">
    <v-card max-width="700" color="rgba(250,250,250,0.8)">
      
        <v-card-title class="title">
          <v-col align="center">
            <v-img style="border-radius: 50%" :max-width="$vuetify.breakpoint.mdAndUp ? '200' : '100'" src="https://avatars2.githubusercontent.com/u/39635641" class="elevation-4"/>
          </v-col>
          <v-col align="center" id="_name">
            <v-card-text  :class="$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline'">Hi, I'm Alex</v-card-text>
          </v-col>
        </v-card-title>
        <v-spacer />
        <v-responsive max-width="600">
        <v-card-text color="black" :class="$vuetify.breakpoint.mdAndUp ? 'headline' : 'subtitle-3'">
          I'm a Full-Stack Developer living in Toronto, Canada.
          <br />
          <br />I specialize in building RESTful Api's for enterprise applications, and developing responsive front-ends for mobile and web.
          Most proficient with Node.js, Express, VueJs, Nativescript, Symfony/Laravel, and React.
        </v-card-text>
      </v-responsive>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: "about"
};
</script>
<style lang="scss">
.title {
  display:flex;
}
#_name {
  flex: 3 60%;
}
</style>