<template>
  <v-container class="fill-height justify-center" fluid>
    <v-row justify="center">
      <v-col cols="12" sm="10" md="8" lg="5" class="px-5">
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
            <v-form ref="form">
              <v-text-field outlined v-model="email" label="E-mail" required></v-text-field>
              <v-text-field outlined v-model="subject" label="Subject" required></v-text-field>
            </v-form>
            <v-textarea
              multi-line
              outlined
              v-model="emailSlug"
              label="Body"
              rows="5"
              row-height="25"
              counter
              maxlength="240"
            ></v-textarea>
            <v-btn @click="click">Send</v-btn>

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
    subject: null,
    email: null,
    emailSlug: null
  }),
  methods: {
    click() {
      //
      alert(
        "Email service currently not available - please contact me at alex.zvaniga@gmail.com in the meantime."
      );
      // eslint-disable-next-line
      console.log(`Name: ${this.subject}`); // eslint-disable-next-line
      console.log(`Email: ${this.email}`); // eslint-disable-next-line
      console.log(`EmailSlug: ${this.emailSlug}`);
    }
  }
};
</script>