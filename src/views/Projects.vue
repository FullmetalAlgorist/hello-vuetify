<template>
  <div class="projects">
    <h1 class="subheading grey--text pt-4">My projects:</h1>
     <v-container class="my-5">

  <v-expansion-panel dark>
    <v-expansion-panel-content
      v-for="project in projects"
      :key="project.id">
        <div slot="header">{{ project.title }}</div>
      <v-card>
        <v-card-text>
          <div class="font-weight-bold">Project Due: {{ project.due }}</div>
          <div>{{ project.info }}</div>
        </v-card-text>
      </v-card>
    </v-expansion-panel-content>
  </v-expansion-panel>

   </v-container>
  </div>
</template>
<script>
export default {
  data(){
    return{
      projects: [
        {title: 'hardcode1', due: '1/1/21', info:'dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1, dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1,dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1,dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1,dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1,dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1,dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1dumyinfo1,'},
        {title: 'hardcode2', due: '1/1/21', info:'dumyinfo2dumyinfo2dumyinfo2dumyinfo2dumyinfo2dumyinfo2dumyinfo2dumyinfo2dumyinfo2dumyinfo2dumyinfo2dumyinfo2dumyinfo2dumyinfo2dumyinfo2dumyinfo2dumyinfo2dumyinfo2dumyinfo2dumyinfo2'},
        {title: 'hardcode3', due: '1/1/21', info:'dumyinfo3dumyinfo3dumyinfo3dumyinfo3dumyinfo3dumyinfo3dumyinfo3dumyinfo3dumyinfo3dumyinfo3dumyinfo3dumyinfo3dumyinfo3dumyinfo3dumyinfo3dumyinfo3dumyinfo3dumyinfo3dumyinfo3dumyinfo3'},
        {title: 'hardcode4', due: '1/1/21', info:'dumyinfo4dumyinfo4dumyinfo4dumyinfo4dumyinfo4dumyinfo4dumyinfo4dumyinfo4dumyinfo4dumyinfo4dumyinfo4dumyinfo4dumyinfo4dumyinfo4dumyinfo4dumyinfo4dumyinfo4dumyinfo4dumyinfo4'}
      ]
    }
  },
    computed: {
      
    }
  
}
</script>
