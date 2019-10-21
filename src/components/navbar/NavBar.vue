<template>
  <nav>
    <v-app-bar app flat color="primary">

      <v-app-bar-nav-icon @click="drawer = !drawer"/>

      <v-toolbar-title class="white--text headline">
        <span class="font-weight-light">Vue</span><span>tify</span>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn class="d-none d-sm-flex" :loading="loading" :disabled="loading" @click="upload" >
        Upload
        <v-icon right dark>mdi-cloud-upload</v-icon>
      </v-btn>
      <v-btn class="d-flex d-sm-none" text icon>
        <v-icon right dark>mdi-cloud-upload</v-icon>
      </v-btn>


      <v-btn class="d-none d-sm-flex" text>
        Sign Out
        <v-icon right dark>mdi-exit-to-app</v-icon>
      </v-btn>
      <v-btn class="d-flex d-sm-none" text icon>
        <v-icon right dark>mdi-exit-to-app</v-icon>
      </v-btn>

    </v-app-bar>

    <v-navigation-drawer app v-model="drawer">
      <p>test</p>
      <v-switch label="Dark Mode" v-model="$vuetify.theme.dark"/>
    </v-navigation-drawer>
  </nav>
</template>

<script>
  export default {
    name: "NavBar",
    data() {
      return {
        loading: false,
        dropdown_font: ['Arial', 'Calibri', 'Courier', 'Verdana'],
        drawer: false,
        goDark: true
      }
    },
    methods: {
      upload() {
        this.loading = !this.loading
        setTimeout(() => (this.loading = !this.loading), 3000)
      }
    }
  }
</script>

<style scoped>

</style>