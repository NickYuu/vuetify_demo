<template>
  <v-app>
    <nav-bar/>
    <v-content>
      <router-view/>
    </v-content>
  </v-app>
</template>

<script>
  import NavBar from "./components/navbar/NavBar"

  export default {
    name: 'App',
    components: {
      NavBar
    },
    data: () => ({}),
  }
</script>
