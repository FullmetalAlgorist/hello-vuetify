<template>
    <v-dialog v-model="dialog" max-width="500px">
        <v-btn flat slot="activator" color="grey">
          <v-icon small left>message</v-icon>
          <span class="pl-.5">message</span>
        </v-btn>
  
        <v-card class="c">
            <v-card-title>
                <h2>What?</h2>
            </v-card-title>

<!-- label="What?" is a prop option for textarea to have a little subtitle thing at the top, probably to use instead of title -->
            <v-textarea v-model="message" ></v-textarea>

            <v-btn class="indigo" @click="printM">send</v-btn>
            <v-btn class="indigo" @click="dF">cancel</v-btn>
        </v-card>
    </v-dialog>
</template>
<script>
export default {
    data(){
        return{
            dialog : false,
            message: ''
        }
    },
    methods:{
        printM(){
            console.log(this.message);
            this.dF();
        },
        dF(){
            this.message='';
            this.dialog = false;
        }
    }
}
</script>
<style scoped>
.c{
   background-color: rgba(128, 128, 128, 0.3)
}
</style>

