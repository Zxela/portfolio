<template>
  
        <v-row align="center" justify="center">
          <v-col cols="12" sm="8" md="6 ">
            <v-card color="rgba(250,250,250,0.8)" class="elevation-10 home-card pt-4">
              <v-row>
                <v-card-text>
                  <div class="text-center">
                    <v-col id="myName" class="display-2 font-weight-black">Alex Zvaniga</v-col>
                    <v-col class="display-1 font-weight-normal">Full-Stack Developer</v-col>
                  </div>
                </v-card-text>
              </v-row>
              <v-card-actions class="justify-center pb-5">
                <Tooltip />
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
 
</template>

<script>
import Tooltip from "@/components/TooltipMenu";

export default {
  name: "home",
  components: { Tooltip }
};
</script>
<style lang="scss">
#myName {
  line-height: 10px;
}
</style>
