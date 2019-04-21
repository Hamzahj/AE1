

<template>
    
<div class="row">
 
     
         <div class="column-12">
    <h1>Tourist hotspots for your family</h1>

 <div class="container">
        <ul>
          <li><span class="left_span"></span><span class="right_span"></span>Home</li>
          <li><span class="left_span"></span><span class="right_span"></span>Services</li>
          <li><span class="left_span"></span><span class="right_span"></span>Contact us</li>
        </ul>

    </div>
         
         </div>
     
     
    
  
     
     <div id="cards">

    <div v-for="result in results" class="col-4">
      <div class="card" style="width: 50rem; height:50rem; margin-left:40px;">
 <img :src="result.picture.url" >" 
  <div class="card-body">
   <div>
 
</div>

     <h5 class="card-title">{{result.name}}</h5>
    <h5 class="card-title">{{result.location.name}}</h5>
    <p class="card-text">{{result.summary}}</p>
    <p class="card-text">{{result.location.address}}</p>
        
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
      inst.get('https://api.autoura.com/api/stops/search?group_context=friends&stop_types=tour').then(r => {
        this.results = r.data.response;
      }).catch(e => {
        console.log(e);
      })
    }
  }
  
  
  
  
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body {
  background-color: lightblue;
}


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
