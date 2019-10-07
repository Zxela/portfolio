<template>
  <v-container class="fill-height justify-center" fluid>
    <v-row justify="center">
      <v-col cols="12" sm="10" md="8" lg="5" class="px-5">
        <v-card color="rgba(250,250,250,0.8)" class="px-5 pb-2 mt-12">
          <v-responsive max-width="700">
            <v-card-title>
              <v-card-text align="center" :class="$vuetify.breakpoint.mdAndUp ? 'display-2' : 'display-1'" class="font-weight-black">Contact Me</v-card-text>
            </v-card-title>
            <v-divider />
            <v-spacer />
            <v-form ref="form">
              <v-text-field outlined v-model="name" :counter="10" label="Name" required></v-text-field>

              <v-text-field outlined v-model="email" label="E-mail" required></v-text-field>
            </v-form>
            <v-textarea
              multi-line
              outlined
              v-model="emailSlug"
              label="Email Body"
              rows="3"
              autogrow
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
    name: null,
    email: null,
    emailSlug: null
  }),
  methods: {
    click() {
      // eslint-disable-next-line
      console.log(`Name: ${this.name}`); // eslint-disable-next-line
      console.log(`Email: ${this.email}`); // eslint-disable-next-line
      console.log(`EmailSlug: ${this.emailSlug}`);
    }
  }
};
</script>