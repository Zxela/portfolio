<template>
  <div>
    <v-navigation-drawer v-model="drawer" app clipped>
      <v-list dense>

        <v-list-item v-for="(item, i) in items"
            :key="i" @click="$router.push(item.to)">
          <v-list-item-action>
            <v-icon>{{item.icon}}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>{{item.text}}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app clipped-left>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Application</v-toolbar-title>

    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  data: () => ({
    drawer: null,
    items: [
      {
        to: "/",
        text: "Home",
        icon: "mdi-home"
      },
      {
        to: "/about-me",
        text: "About Me",
        icon: "mdi-view-dashboard"
      },
      {
        to: "/my-work",
        text: "My Work",
        icon: "mdi-view-dashboard"
      },
      {
        to: "/contact-me",
        text: "Contact Me",
        icon: "mdi-contact-mail"
      }
    ]
  })
};
</script>

<style>
</style>