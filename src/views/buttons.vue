<template>
 <div class="buttons">
   <h1>Buttons Page</h1>
<v-btn class="pink white--text">hi</v-btn>
<v-btn dark depressed color="pink">DEPRESSED</v-btn>
<v-btn dark color="pink" flat>FLAT</v-btn>

<v-btn small depressed class="pink white--text">
  <v-icon small left>email</v-icon>
  <span>email</span>
</v-btn>
<v-btn large depressed color="indigo">
  <span>shop</span>
  <v-icon large right>shopping_basket</v-icon>
</v-btn>
  
<v-btn fab large depressed color="pink">
  <v-icon large>favorite</v-icon>
</v-btn>
<v-btn fab  depressed color="indigo">
  <v-icon >favorite</v-icon>
</v-btn>
<v-btn fab small depressed color="blue">
  <v-icon small>favorite</v-icon>
</v-btn>

 </div>
</template>

<script>


  export default {
    components: {
    
    }
  }
</script>
