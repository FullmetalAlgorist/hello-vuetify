<template>
    <v-dialog max-width="600px" v-model="popup">
        <v-btn slot="activator" outline>Add new project</v-btn>
        <v-card class="card c">
            <v-card-title>
                <h2>Add a new Project:</h2>
            </v-card-title>
            <v-card-text>
                <v-form class="px-3" ref="form">
                <v-text-field label="Title" v-model="title" prepend-icon="folder" :rules="rules"></v-text-field>
               <v-textarea label="Information" v-model="content" prepend-icon="edit" :rules="rules"></v-textarea>
               <v-menu>
                   <v-text-field :value="formattedDate" slot="activator" label="Due date" prepend-icon="date_range"></v-text-field>
                <v-date-picker v-model="due"></v-date-picker>
               </v-menu>
               <v-spacer></v-spacer>
               <v-btn @click="Sub" class="mx-0 mt-3 indigo">Submit</v-btn>
               <v-btn @click="pF" class="ml-2 mt-3 indigo">Cancel</v-btn>
               </v-form>
                </v-card-text>
        </v-card>
    </v-dialog>
</template>
<script>
import format from 'date-fns/format'
export default {
    data(){
        return{
            title: '',
            content: '',
            popup: false,
            due: null,
            rules: [
                v => v.length >= 3 || 'Minimum length is 3 characters'
            ]
        }
    },
    methods:{
        Sub(){
            if(this.$refs.form.validate()){
                //create new project with this info before deleting it
                console.log(this.title, this.content);
                this.pF();
            }
        },
        pF(){
            this.popup = false;
            this.title = '';
            this.content = '';
        }
    },
        computed:{
            formattedDate(){
                console.log(this.due);
                return this.due ? format(this.due, 'MMM Do YYYY') : ''
            }
        }
}
</script>
<style scoped>
.c{
   background-color: rgba(128, 128, 128, 0.6)
}
</style>

