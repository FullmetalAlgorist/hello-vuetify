<template>
  <v-app dark class="">
    <v-content class="mx-4 mb-4">
      <toolbar></toolbar>
      <!--    <overlay></overlay> -->
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
import Toolbar from './components/toolbar'
import Overlay from './components/overlay-menu'
export default {
  name: 'App',
  components: {
    Toolbar,
    overlay: Overlay
  },
  data () {
    return {
      //
    }
  }
}
</script>
