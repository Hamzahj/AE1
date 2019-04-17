<template>
  <div id="app">
   <ShowData/>
  </div>
</template>

<script>
import ShowData from './components/ShowData.vue'

export default {
  name: 'app',
  components: {
    ShowData
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
  
}


#cards{
   margin-left:100px; 
  width:50rem;
 float:left;
    border: dashed;
}

*{
  box-sizing: border-box;
}

body{
  background-image: linear-gradient(to left, #BDBBBE 0%, #9D9EA3 100%), radial-gradient(88% 271%, rgba(255, 255, 255, 0.25) 0%, rgba(254, 254, 254, 0.25) 1%, rgba(0, 0, 0, 0.25) 100%), radial-gradient(50% 100%, rgba(255, 255, 255, 0.30) 0%, rgba(0, 0, 0, 0.30) 100%);
 background-blend-mode: normal, lighten, soft-light;
  height: 850px;
}

.container{
  width: 100%;
}

.container ul{
  width: 600px;
  margin: 50px auto;

}

.container ul li{
  font-family: tahoma,arial;
  display: inline-block;
  text-align: center;
  width: 150px;
  height: 50px;
  padding-top: 12px;
  font-size: 20px;
  background-color: #1e272e;
  color: #808e9b;
  margin: 0;
  position: relative;
  cursor: pointer;

}

.container ul li .left_span{
  position: absolute;
  top: 0;
  left: 0;
  width: 6px;
  height: 0%;
  background-color: #d2dae2;
}

.container ul li .right_span{
  position: absolute;
  top: 0;
  right: 0;
  width: 6px;
  height: 0%;
  background-color: #d2dae2;
}


.container ul li:hover span{
  height: 100%;
  transition: all .5s ease-in-out;
}

.container ul li:hover{
  color: #d2dae2;
  /* padding-top: 15px; */
  transition: all .5s ease-in-out;
}


.row, 
.column {
    box-sizing: border-box;
}

.row:before,
.row:after {
    content: " ";
    display: table;
}

.row:after {
    clear: both;
}

.column {
    position: relative;
    float: left;
    display: block;
}

.column + .column {
    margin-left: 1.6%;
}

.column-1 {
    width: 6.86666666667%;
}

.column-2 {
    width: 15.3333333333%;
}

.column-3 {
    width: 23.8%;
}

.column-4 {
    width: 32.2666666667%;
}

.column-5 {
    width: 40.7333333333%;
}

.column-6 {
    width: 49.2%;
    position: absolute;
  margin-left:500px;
    padding-top: 10;
   padding-right: 10;
    padding-bottom: 10;
  padding-left: 10;
  width: 100%;
  height: 100%;
  background-color: #ccc;
  border-radius: 3px;
  padding-left:700px;
    
}

.column-7 {
    width: 57.6666666667%;
}

.column-8 {
    width: 66.1333333333%;
}

.column-9 {
    width: 74.6%;
}

.column-10 {
    width: 83.0666666667%;
}

.column-11 {
    width: 91.5333333333%;
}

.column-12 {
    width: 100%;
    margin-left: 0;
    margin-right:0;
    height:100%;

 
             
}




@media only screen and (max-width: 550px) {
    .column-1, 
    .column-2, 
    .column-3, 
    .column-4, 
    .column-5, 
    .column-6, 
    .column-7, 
    .column-8, 
    .column-9, 
    .column-10, 
    .column-11, 
    .column-12 {
        float: none;
        width: auto;
    }
  
    .column + .column {
        margin-left: 0;
    }
}




body {
    padding: 20px;
}

.card{
    margin-left:200px;

}
.column {
    background: #eee;
    border: 1px solid #ccc;
    border-radius: 4px;
    color: #777;
    padding: 5px;
    min-height: 30px;
    text-align: center;
}

.row {
    margin-bottom: 10px;
}

.row:last-child {
    margin-bottom: 0;
}

.column .column {
    color: #eee;
    background: #333;
    border-color: #000;
}

.p {
  font-size: 14px;
  text-align: center;
  padding-top: 100px;
}

</style>
