<template>
  <v-app dark class="">
    <v-content class="mx-4 mb-4">
      <toolbar></toolbar>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
import Toolbar from './components/toolbar'
export default {
  name: 'App',
  components: {
    Toolbar
  },
  data () {
    return {
      //
    }
  }
}
</script>
