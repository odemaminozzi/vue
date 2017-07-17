<template>
  <div id="app">
   <md-card>
   <md-card-header>
 <div id="md-title">
 Material design
 </div>
 <div id="md-subhead">
by coding amedeominozzi.com
 </div>

</md-card-header>
   
   <md-card-content>
   <md-button class ="md-raised md-primary" v-on:click="fillTable()">fillTable
   
   </md-button>
   <md-button class ="md-raised md-primary" v-on:click="clearTable()">clearTable
   
   </md-button>

</md-card-content>


   <md-table>
   <md-table-header>

   


   <md-table-row>
   <md-table-head>First Name</md-table-head>
   <md-table-head>Last Name</md-table-head>
   <md-table-head>Email</md-table-head>

          


   </md-table-row>

      </md-table-header>
   
   <md-table-body>

     
       <md-table-row v-for="contact in contacts">
       <md-table-cell>{{contact.firstname}}</md-table-cell>
       <md-table-cell>{{contact.lastname}}</md-table-cell>
       <md-table-cell>{{contact.email}}</md-table-cell>
       
       
       </md-table-row>
      

   </md-table-body>




   
   








   </md-table>
   </md-card>
  </div>
</template>

<script>
import Hello from './components/Hello'

export default {
  name: 'app',
  data: function(){
    return{
      contacts:[]
    }
  },
  methods: {
    fillTable: function(){
      this.contacts.push({firstname:'Amedeo', lastname:'Minozzi',email:'amedeominozzi@gmail.com'});
      this.contacts.push({firstname:'Emilio', lastname:'Passananti', email:'emiliopassananti@gmail.com'});
    },
  clearTable : function(){
    this.contacts.splice(0, this.contacts.length);
  }
  
  
}
}

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  margin-left: 30px;
  margin-right: 30px;
}
</style>
