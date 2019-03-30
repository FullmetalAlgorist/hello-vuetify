<template>
  <div class="home">
    <h1 class="subheading grey--text pt-4">HOME</h1>
      <v-container class="my-3">

        <v-layout row class="mb-3">
          <v-tooltip top>
          <v-btn small flat color="grey" @click="sortBy('title')" slot="activator">
            <v-icon left small>folder_open</v-icon>
            <span class="caption text-lowercase">By project name</span>
          </v-btn>
          <span>Sort projects by name</span>
          </v-tooltip>
          <v-tooltip top>
          <v-btn small flat color="grey" @click="sortBy('person')" slot="activator">
            <v-icon left small>person</v-icon>
            <span class="caption text-lowercase">By person</span>
          </v-btn>
<span>Sort projects by person</span>
          </v-tooltip>
        </v-layout>

     <v-card v-for="project in projects" :key="project.id" flat>
       <v-layout row wrap :class="`pa-3 project ${project.status}`"> 
         <v-flex xs6 md6 class="pr-1 py-1">
           <div class="caption grey--text">Title</div>
           <div>{{ project.title }}</div>
         </v-flex>
         <v-flex xs6 sm4 md2>
            <div class="caption grey--text">Person</div>
            <div>{{ project.person }}</div>
         </v-flex>
           <v-flex xs6 sm4 md2>
            <div class="caption grey--text">Due Date</div>
            <div>{{ project.due }}</div>
         </v-flex>
          <v-flex xs6 sm4 md2>

          <div class="right">
            <v-chip small :class="`${project.status} white--text caption my-2`">{{ project.status }}</v-chip>
          </div> 
           <div></div>
         </v-flex>
       </v-layout>
       <v-divider></v-divider>
     </v-card>
        </v-container>
  </div>
</template>

<script>


  export default {
  
    data(){
      return {
         projects: [
        { title: 'Design a new website', 
        person: 'The Net Ninja', 
        due: '1st Jan 2019', 
        status: 'ongoing', 
        content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt consequuntur eos eligendi illum minima adipisci deleniti, dicta mollitia enim explicabo fugiat quidem ducimus praesentium voluptates porro molestias non sequi animi!'
        ,avatar: 'https://images.unsplash.com/photo-1537815749002-de6a533c64db?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1445&q=80'},
        { title: 'Code up the homepage', person: 'Chun Li', due: '10th Jan 2019', status: 'complete', content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt consequuntur eos eligendi illum minima adipisci deleniti, dicta mollitia enim explicabo fugiat quidem ducimus praesentium voluptates porro molestias non sequi animi!'},
        { title: 'Design video thumbnails', person: 'Ryu', due: '20th Dec 2018', status: 'complete', content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt consequuntur eos eligendi illum minima adipisci deleniti, dicta mollitia enim explicabo fugiat quidem ducimus praesentium voluptates porro molestias non sequi animi!'},
        { title: 'Create a community forum', person: 'Gouken', due: '20th Oct 2018', status: 'overdue', content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt consequuntur eos eligendi illum minima adipisci deleniti, dicta mollitia enim explicabo fugiat quidem ducimus praesentium voluptates porro molestias non sequi animi!'},
      ]
      }
    },
    methods: {
      sortBy(prop){
          this.projects.sort((a,b) => a[prop] < b[prop] ? -1 : 1)
      }
}
  }
  
</script>
<style scoped>
.project.complete {
  border-left: 4px solid #3cd1c2;
}
.project.ongoing{
  border-left: 4px solid orange;
}
.project.overdue{
  border-left: 4px solid tomato;
}
.v-chip.complete{
  background:#3cd1c2;
}
.v-chip.ongoing{
background: orange;
}
.v-chip.overdue{
  background:  tomato;
}
</style>
