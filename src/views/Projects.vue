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
           <div class="mx-4 mt-1" >
              <div class="font-weight-bold">Project Due: {{ project.due }}</div>
           <v-card-text >{{ project.info }}
             </v-card-text>
          </div> 
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
        {title: 'Figure out why cats are evil', due: '1/1/21', info:'Cats are a globally invasive species. They kill millions of birds each year in Wisconsin alone. Cats feast on endangered North American ground-nesting birds such as the California clapper rail, least tern, and piping plover, any one of which is cuter than a laundry basket full of kittens. A study in the D.C. area a few years ago showed that in some neighbourhoods (neighbourhoods in which a lot of people who really ought to know better let their beasts roam free), outdoor cats eat basically all juvenile birds as soon as they fledge.'},
        {title: 'Write nonprofit proposal', due: '1/1/21', info:"NPO's challenges primarily stem from lack of funding. Funding can either come from within the organization, fundraising, donations, or from the federal government. When cutbacks are made from the federal government, the organization suffers from devolution. This term describes when there is a shift of responsibility from a central government to a local, subnational authority. The shift is due to the loss of funds; therefore, resulting in changes of responsibilities in running programs. Because of this frequent challenge, management must be innovative and effective in the pursuit of success."},
        {title: 'Calculate budget', due: '1/1/21', info:'There are several guidelines to use when allocating money for a budget as well. Past spending is one of the most important priorities; a critical step in most personal budgeting strategies involves keeping track of expenses via receipts over the past month so that spending for the month can be reconciled with budgeted spending for the next month. Any of the following allocation guidelines may be used; choose one that will work well with your situation.'},
        {title: 'Publish bibliography', due: '1/1/21', info:'A bibliographer is a person who describes and lists books and other publications, with particular attention to such characteristics as authorship, publication date, edition, typography, etc. A person who limits such efforts to a specific field or discipline is a subject bibliographer A bibliographer, in the technical meaning of the word, is anyone who writes about books. But the accepted meaning since at least the 18th century is a person who attempts a comprehensive account—sometimes just a list, sometimes a fuller reckoning—of the books written on a particular subject. In the present, bibliography is no longer a career, generally speaking; bibliographies tend to be written on highly specific subjects and by specialists in the field.'}
      ]
    }
  },
    computed: {
      
    }
  
}
</script>
