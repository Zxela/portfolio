<template>
  <v-container class="fill-height justify-center" fluid>
    <v-row justify="center">
      <v-col cols="12" sm="10" md="8" lg="6">
        <v-card color="" class="px-5 pb-2">
          <v-responsive>
            <v-card-title>
              <v-card-text
                align="center"
                :class="$vuetify.breakpoint.mdAndUp ? 'headline' : 'title'"
                class="font-weight-black"
              >Contact Me</v-card-text>
            </v-card-title>

            <v-spacer />
            <v-form action="https://formspree.io/alex.zvaniga@gmail.com" method="POST" ref="form">
              <v-text-field
                outlined
                v-model="name"
                :error-messages="nameErrors"
                label="Name"
                name="name"
                required
                @input="$v.name.$touch()"
                @blur="$v.name.$touch()"
              ></v-text-field>
              <v-text-field
                outlined
                v-model="email"
                :error-messages="emailErrors"
                label="Email"
                name="email"
                required
                @input="$v.email.$touch()"
                @blur="$v.email.$touch()"
              ></v-text-field>
              <v-textarea
                multi-line
                outlined
                v-model="emailSlug"
                :error-messages="emailSlugErrors"
                label="Body"
                name="message"
                rows="5"
                row-height="25"
                counter
                maxlength="240"
                @input="$v.emailSlug.$touch()"
                @blur="$v.emailSlug.$touch()"
              ></v-textarea>
              <v-btn type="submit" @click="click" text outlined block class="elevation-1">Send</v-btn>
            </v-form>
            <v-card-actions></v-card-actions>
          </v-responsive>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import { validationMixin } from "vuelidate";
import { required, maxLength, email } from "vuelidate/lib/validators";

export default {
  name: "contact",
  mixins: [validationMixin],
  validations: {
    name: { required, maxLength: maxLength(20) },
    email: { required, email },
    emailSlug: { required, maxLength: maxLength(240) }
  },
  data: () => ({
    name: "",
    email: "",
    emailSlug: ""
  }),
  computed: {
    nameErrors() {
      const errors = [];
      if (!this.$v.name.$dirty) return errors;
      !this.$v.name.maxLength &&
        errors.push("Name must be at most 20 characters long");
      !this.$v.name.required && errors.push("Name is required.");
      return errors;
    },
    emailErrors() {
      const errors = [];
      if (!this.$v.email.$dirty) return errors;
      !this.$v.email.email && errors.push("Must be valid e-mail");
      !this.$v.email.required && errors.push("E-mail is required");
      return errors;
    },
    emailSlugErrors() {
      const errors = [];
      if (!this.$v.email.$dirty) return errors;
      !this.$v.emailSlug.required && errors.push("E-mail is required");
      !this.$v.emailSlug.maxLength &&
        errors.push("Name must be at most 10 characters long");
      return errors;
    }
  },
  methods: {
    click(ev) {
      this.$v.$touch();
      if (this.nameErrors.length || this.emailErrors.length || this.emailSlugErrors.length) {
        ev.preventDefault()
      } else {
        return ev;
      }
      
    }
  }
};
</script>