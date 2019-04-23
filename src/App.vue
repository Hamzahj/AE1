<template>
  <div id="app">
     
   <div class="container">
       
<div class="text">
   <nav id="navbar">
       
       <ul>  <router-link :to="'/'"> <li><span class="left_span"></span><span class="right_span"></span><h2>Home</h2></li>
                
            </router-link>
           
           
            <router-link :to="'/add'">
               <li><span class="left_span"></span><span class="right_span"></span><h2>Tourism</h2></li>
             </router-link>
           </li>
       </ul>
   </nav>
 </div>
   </div>
   <router-view></router-view>
   
  </div>
  
</template>

<script>
import ShowData from './components/ShowData.vue';


export default {
  name: 'app',
  components: {
    ShowData
  }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
}

.button {
  width: 110px;

  }
  .button {
  color: #fff;
  text-align:center;
  line-height:40px;
  height: 40px;
  border-radius:20px;
  background: linear-gradient(90deg, green, blue, green,black)  center / cover;
  background-size: 400% 400%;
  animation: AnimationName 2.5s ease infinite;
  }
  @keyframes AnimationName { 
  0%{background-position:100% 50%}
  100%{background-position:0% 50%}
  
  }
  
header {
     background: url(https://i.postimg.cc/v8zM41BJ/adventure-beautiful-boardwalk-235734.jpg) no-repeat fixed center;
    display: flex;
    justify-content: center;
    align-items: center;
}
#navbar{
    opacity: 0.8;
    
}
.h2{
    color:white;
}

#one {
    background: url(http://www.bingwallpaperhd.com/wp-content/uploads/2018/09/ArcticHenge.jpg) no-repeat fixed center;
    background-size: cover;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
}

#one .two h1 {
    background: rgba(36, 42, 45, 0.5);
    color: #fff;
    padding: 1em;
}



#three {
    background: url(http://www.bingwallpaperhd.com/wp-content/uploads/2018/07/FujiMilkyway0.jpg ) no-repeat fixed center;
    background-size: cover;
    height: 50vh;

    display: flex;
    align-items: center;
    justify-content: center;
}



#four {
    background-image: url('https://www.wildlifearchives.com/wp-content/uploads/2017/05/aurora-borealis-most-beautiful-picture-of-the-day-may-most-beautiful-picture-14949436938k4gn-1280x720.jpg');
    background-size: cover;
    height: 100vh;

    display: flex;
    align-items: center;
    justify-content: center;
}

#four .text, #three .text{
    width: 30em;
    text-align: center;
  color: #fff;
  line-height: 1.5;
}


.two{
  margin: 0 auto;
  width: 100%;
}


@media (min-width: 576px) {
  
}

@media screen and (min-width:768px) {

    #one {
        height: 100vh;

    }
}


@media (min-width: 992px) {
  
}

@media screen and (min-width:1024px) {


    #one {
        height: 100vh;

    }
}



@media screen and (min-width:1920px) {

}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
 -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

  background-image: url('http://www.bingwallpaperhd.com/wp-content/uploads/2019/02/RavenWolf.jpg');
  background-repeat: repeat;
  background-size: auto;

  
}

.text-center{
   color:black;
   h1:black;
}
.card-title{
    color:white;
    
}
.card-text{
    color:white;
    
}
.card-body{
    
    background-color:black;
    opacity:0.7;
}
#cards{
   margin-left:100px; 
  width:10rem;
 float:right;

}

.left-span{
    padding: 100px 400px; 
}


.container{
    padding-top:5rem;
  width: 100%;
  height:100%;
}

.container ul{
  width: 100%;
  margin: 100px auto;

}

.container ul li{
  font-family: tahoma,arial;
  display: inline-block;
  text-align: center;
  width: 100%;
  height: 50px;

  font-size: 20px;
background: rgba(36, 42, 45, 0.5);
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
  background-color: white;

}

.container ul li .right_span{
  position: absolute;
  top: 0;
  right: 0;
  width: 6px;
  height: 0%;
  background: rgba(36, 42, 45, 0.5);
}


.container ul li:hover span{
  height: 100%;
  transition: all .5s ease-in-out;
   color: #fff;
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
  overflow:hidden;
    margin-right:500px;
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




.left-span{
    padding: 100px 400px; 
}


.container{
  width: 100%;
}

.container ul{
  width: 100%;
  margin: 100px auto;

}

.container ul li{
  font-family: tahoma,arial;
  display: inline-block;
  text-align: center;
  width: 100%;
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
 
  transition: all .5s ease-in-out;
}



.ui-cards {
     margin-top:100px;
    margin-left:100px;
      margin-right:100px;
        margin-bottom:100px;
    
  text-align: center;

;


}
.ui-cards:hover .ui-card {
  opacity: 0.4;
}
.ui-cards:hover .ui-card:hover {
  -webkit-transform: scale(1.1);
          transform: scale(1.1);
  opacity: 1;
  
}

.ui-card {
  box-shadow: 0 2px 30px rgba(0, 0, 0, 0.2);
  border-radius: 100px;
  background: lightblue;
  padding: 4rem 1rem;
  transition: 300ms opacity, 300ms -webkit-transform;
  transition: 300ms opacity, 300ms transform;
  transition: 300ms opacity, 300ms transform, 300ms -webkit-transform;
}





</style>
