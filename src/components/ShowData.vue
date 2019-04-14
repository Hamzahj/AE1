<template>
<div class="row">
    
     <div class="col-12">  <h1 class='text-center'>Places that Visit</h1>   </div>
    <div v-for="result in results" class="col-4">
      <div class="card" style="width: 18rem;">
  <img class="card-img-top" src="" alt="Card image cap">
  <div class="card-body">
    <h5 class="card-title">{{result.name}}</h5>
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
    </div>
    <!-- ./col-6 -->
    
  

</div>
<!-- ./row -->
    
    
    
   
  </div>
</template>

<script>

  import { AUTORA_KEY } from '../config';
  import axios from 'axios';


  export default {
    name: 'ShowData',
    data: function() {
      return {
        key: AUTORA_KEY,
        results: [],
        show: false
      }
    },
    mounted: function() {
      

      const inst = axios.create({ headers: { 'Authorization': 'Bearer ' + this.key } })
      inst.get('https://api.autoura.com/api/stops/search?group_context=friends&stop_types=food').then(r => {
        this.results = r.data.response;
      }).catch(e => {
        console.log(e);
      })
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>



<!--<template>
   <div class="card">
  <ul class="list-group list-group-flush">
    <li 
    v-bind:key="index"
    v-for="(brew, index) in brews"
     class="list-group-item"
    
    > {{index}}, {{brew.name}}, {{brew.state}}</li>

  </ul>   
    
    </div>
    
</template>

<script>
    
    export default{
        name:"brewlist",
        props:{
            brews: Array
        }
    }
    
    
</script>

<style lang="scss" scoped>
    
  
     .brew-list{
       overflow-y: scroll;
       
      height: 95vh;
     }
     
     li{
        &:hover{
         background-color:darkgrey;
       }
     }


       
       
       </style>
