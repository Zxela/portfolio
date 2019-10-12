<template>
  <v-container class="fill-height justify-center">
    <v-row justify="center">
      <v-col cols="11" sm="7" md="6" lg="6" xl="4" class="px-5">
        <v-card color="">
          <v-card-title class="title-box">
            <v-col align="center">
              <v-img
                style="border-radius: 50%"
                :max-width="$vuetify.breakpoint.mdAndUp ? '200' : '150'"
                src="https://avatars2.githubusercontent.com/u/39635641"
                class="elevation-4"
              />
            </v-col>
            <v-col align="center" id="_name">
              <v-card-text :class="$vuetify.breakpoint.mdAndUp ? 'headline' : 'title'">Hi, I'm Alex</v-card-text>
            </v-col>
          </v-card-title>
          <v-spacer />
          <v-responsive>
            <v-card-text color="black" :class="$vuetify.breakpoint.mdAndUp ? 'body-1' : 'body-2'">
              I'm a Full-Stack Developer living in Toronto, Canada.
              <br />
              <br />I specialize in building RESTful API's for enterprise applications, and developing responsive front-ends for mobile and web.
            </v-card-text>
          </v-responsive>
          <v-card-actions></v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "about",
  data: () => ({})
};
</script>
<style lang="scss">
.title-box {
  display: flex;
}
#_name {
  flex: 2 60%;
}
</style>