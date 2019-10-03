<template>
  <v-img
    height="100vh"
    gradient="to top, rgb(189,195,199,.75), rgba(44,62,80,.75)"
    src="https://images.pexels.com/photos/160107/pexels-photo-160107.jpeg"
  >
    <v-content id="content" class="fill-height">
      <v-container class="fill-height" fluid clipped-left>
        <v-row align="center" justify="center">
          <v-col cols="12" sm="8" md="4">
            <v-card color="rgba(250,250,250,0.8)" class="elevation-10 home-card">
              <v-row>
                <v-card-text>
                  <div class="text-center">
                    <v-col class="display-2">Alex Zvaniga</v-col>
                    <v-col class="display-1">Full-Stack Developer</v-col>
                  </div>
                </v-card-text>
              </v-row>
              <v-card-actions class="justify-center pb-5">
                <Tooltip />
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-img>
</template>

<script>
import Tooltip from "@/components/TooltipMenu";

export default {
  name: "home",
  components: { Tooltip }
};
</script>
<style lang="scss">
.home-card {}
</style>
