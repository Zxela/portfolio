<template>
  <v-container class="fill-height">
    <v-row justify="center" align="center">
      <v-col cols="12" sm="8" md="6" lg="4" class="px-5">
        <v-card color="rgba(250,250,250,0.8)" class="elevation-12">
          <v-row>
            <v-card-text>
              <div class="text-center">
                <v-col id="myName" class="font-weight-black display-1">Alex Zvaniga</v-col>
                <v-col class="font-weight-normal headline">Full-Stack Developer</v-col>
              </div>
            </v-card-text>
            <v-divider />
          </v-row>
          <v-card-actions class="justify-center pb-5">
            <Tooltip />
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Tooltip from "@/components/TooltipMenu";

export default {
  name: "home",
  components: { Tooltip }
};
</script>
<style lang="scss">
</style>
