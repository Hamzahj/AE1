<template>
  
  
    
<div class="row">
    
     <div class="column-12">  <h1 class='text-center'>Places to Visit</h1>   </div>
    <div v-for="result in results" class="col-6">
      <div class="card" style="width: 40rem;">
 

<div class="column-5">
<div class="ui-cards"style="width: 500px; height: 500px;">
 
  <div class="ui-card"style="width: 500px; height: 500px;">
     <img :src="result.picture.url"style="width: 20rem; height: 10rem;"> 
    <h1>{{result.name}}</h1>
 {{result.location.name}}</h1>
<p>{{result.summary}}</P>
  <p>{{result.location.address}}</P></div>
  <div class="button">
  <div>Book now</div>
</div>
</div>

</div>

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

