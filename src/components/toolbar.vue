<template>
    <div class="toolbar">
        <v-toolbar flat app>
              <v-toolbar-side-icon @click="drawer =!drawer"></v-toolbar-side-icon>
            <v-toolbar-title class="text-uppercase grey--text">
                <span class="font-weight-light">Todo</span>
                <span>Ninja</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn flat color="grey">
                <span>Sign Out</span>
                <v-icon right>exit_to_app</v-icon>
            </v-btn>
        </v-toolbar>

        <v-navigation-drawer app v-model="drawer" class="indigo" mobile-break-point="50000">
            <v-toolbar-side-icon class="mt-2 ml-3" @click="drawer =!drawer"><v-icon>close</v-icon></v-toolbar-side-icon>
            <v-layout column align-center>
                
                <v-flex class="mt-3">
                    <v-avatar size="200">
                        <img src="https://images.unsplash.com/photo-1537815749002-de6a533c64db?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1445&q=80" alt="">
                    </v-avatar>
                    <p class="white--text subheading mt-1 mariah">
                        Mariah
                    </p>
                </v-flex>
                <v-flex class="mt-3 mb-3">
                    <popup></popup>
                </v-flex>
            </v-layout>
            <v-list>
                <v-list-tile v-for="link in links" :key="link.text" router :to="link.route">
                    <v-list-tile-action>
                        <v-icon class="white--text">{{ link.icon }}</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                        <v-list-tile-title class="white--text">{{ link.text }}</v-list-tile-title>
                    </v-list-tile-content>
                </v-list-tile>
            </v-list>
        </v-navigation-drawer>
    </div>
</template>
<script>
import Popup from './popup'

export default {
    data(){
        return {
            drawer: false,
            links: [
                { icon: 'dashboard', text: 'Dashboard', route: '/'},
                { icon: 'folder', text: 'My Projects', route: '/projects'},
                { icon: 'person', text: 'Team', route: '/team'}
            ]
        }
    },
    components:{
        popup: Popup,
        
    }
    
}
</script>
<style lang="scss" scoped>
.mariah{
    text-align: center;
}
img{
  object-fit:cover; 
}
</style>
