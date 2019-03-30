<template>
  <div class="team">
    <h1 class="subheading grey--text pt-4">Meet the team:</h1>
  <v-container class="my-5">
<!-- maybe popup component with v-model="dialog" -->

<v-layout row wrap class="text-xs-center">
  <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.id">
    <v-card class="light  ma-2">
      <v-responsive class="pt-4">
        <v-avatar size="200" class="grey lighten-4">
          <img :src="person.avatar" alt="">
        </v-avatar>
      </v-responsive>
    <v-card-text>
      <div class="subheading">{{ person.name }}</div>
      <div class="subheading">{{ person.role }}</div>
    </v-card-text>
   <message> </message>
    </v-card>
  </v-flex>
</v-layout>
    </v-container>
  </div>
</template>
<script>
import Message from '../components/message'
export default {
  data(){
    return{
      dialog: false,
      team: [
        { name: 'Mariah', role: 'Web developer', avatar: 'https://images.unsplash.com/photo-1537815749002-de6a533c64db?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1445&q=80' },
        { name: 'Ryu', role: 'Graphic designer', avatar: 'https://images.unsplash.com/photo-1460152129645-978c4acde887?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1867&q=80' },
        { name: 'Chun Li', role: 'Web developer', avatar: 'https://images.unsplash.com/photo-1453227588063-bb302b62f50b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1650&q=80' },
        { name: 'Gouken', role: 'Social media maverick', avatar: 'https://images.unsplash.com/photo-1458724338480-79bc7a8352e4?ixlib=rb-1.2.1&auto=format&fit=crop&w=1650&q=80' },
        { name: 'Yoshi', role: 'Sales guru', avatar: 'https://images.unsplash.com/photo-1424291714008-af2fb994f4c6?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1647&q=80'}
      ]
    }
  },
  methods:{
 
  },
  components:{
    message: Message
  }
}
</script>
<style scoped>
img{
  object-fit:cover; 
}
.light{
  background-color: rgb(101, 99, 99);
}
.dial{
  opacity: 20%;
}

</style>
