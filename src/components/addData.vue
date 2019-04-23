<template>
    
<div class="row">
    
     <div class="column-12">  <h1 class='text-center'>Places to Visit</h1>   </div>
    <div v-for="result in results" class="col-6">
      <div class="card" style="width: 40rem;">
 <img :src="result.picture.url" > 
  <div class="card-body">


    <h5 class="card-title">{{result.name}}</h5>
    <h5 class="card-title">{{result.location.name}}</h5>
    <p class="card-text">{{result.summary}}</p>
    <p class="card-text">{{result.location.address}}</p>







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


</style>

