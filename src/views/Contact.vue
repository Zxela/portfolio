<template>
  <v-container class="fill-height justify-center" fluid>
    <v-row justify="center">
      <v-col cols="12" sm="10" md="8" lg="4" class="px-5">
        <v-card color="rgba(250,250,250,0.8)" class="px-5 pb-2 mt-12">
          <v-responsive max-width="700">
            <v-card-title>
              <v-card-text
                align="center"
                :class="$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline'"
                class="font-weight-black"
              >Contact Me</v-card-text>
            </v-card-title>
            <v-divider />
            <v-spacer />
            <v-form action="https://formspree.io/alex.zvaniga@gmail.com" method="POST" ref="form">
              <v-text-field outlined v-model="name" label="Name" name="name" required></v-text-field>
              <v-text-field outlined v-model="email" label="Email" name="email" required></v-text-field>
              <v-textarea
                multi-line
                outlined
                v-model="emailSlug"
                label="Body"
                name="message"
                rows="5"
                row-height="25"
                counter
                maxlength="240"
              ></v-textarea>
              <v-btn type="submit">Send</v-btn>
            </v-form>
            <v-card-actions></v-card-actions>
          </v-responsive>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "contact",
  data: () => ({
    name: null,
    email: null,
    emailSlug: null
  }),
  methods: {
    click() {}
  }
};
</script>