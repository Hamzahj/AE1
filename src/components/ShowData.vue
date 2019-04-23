
<template>

    
<div class="row">
 
     
         <div class="column-12">
   <section id="one" class="section">
 
        <div class="text">
            <div class="two">
                <h1>Welcome to Javed tourism, powered by the Autora API</h1>
            </div>
        </div>
    </section>

    <section id="three">
      <div class="text">
        <div class="two">
            <h2>Tourist hot spots</h2>
            <p>To find out more details on tourist hot spots in your location, click on the tourism tab</p>
        </div>
      </div>
    </section>

    <section id="four" class="section">
        <div class="text">
            <div class="two">
                <h2>Explore</h2>
                <p>Exploring around a city can never be easier. Find places and activities to enjoy </p>
            </div>
        </div>
    </section>
    
    
    
    </div>



<div class="row">
 
     
         <div class="column-12">
  

</div>


</div>

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

