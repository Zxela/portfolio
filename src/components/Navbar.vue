<template>
  <div>
    <v-navigation-drawer color="grey lighten-3" v-model="drawer" app clipped>
      <v-list dense>

        <v-list-item v-for="(item, i) in items"
            :key="i" @click="click(item)">
          <v-list-item-action>
            <v-icon>{{item.icon}}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>{{item.text}}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      
      </v-list>
    </v-navigation-drawer>

    <v-app-bar color="grey lighten-3" app clipped-left>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="text-capitalize">{{$route.name}}</v-toolbar-title>

    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  data: () => ({
    drawer: false,
    items: [
      {
        to: "/",
        text: "Home",
        icon: "mdi-home"
      },
      {
        to: "/about",
        text: "About Me",
        icon: "mdi-account-tie"
      },
      {
        to: "/projects",
        text: "My Work",
        icon: "mdi-desktop-mac-dashboard"
      },
      {
        to: "/contact",
        text: "Contact Me",
        icon: "mdi-contact-mail"
      },
      {
        to: "https://github.com/zxela",
        text: 'Github',
        icon: 'mdi-github-circle',
      },
      {
        to: "https://www.linkedin.com/in/alexzvaniga/",
        text: 'Linkedin',
        icon: 'mdi-linkedin-box',
      },
      {
        to: "https://resume.creddle.io/resume/2m8wwvhbtlk",
        text: 'Resume',
        icon: 'mdi-file-account',
      }
    ]
  }),
  methods: {
    click(item) {
      if (item.to[0] !== '/') {
        window.location = item.to
      } else {
        this.$router.push(item.to)
      }
    }
  }
};
</script>

<style>
</style>