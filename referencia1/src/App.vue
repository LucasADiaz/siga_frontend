<template>
  <div id="app">
    
    
 <!--    <Test msg="Hola guacho"/> -->
 <!-- <User/> -->
<nav>
<ul>
  <li>
    <router-link to="/test">
      Test
    </router-link> 
  </li>
  <li>
    <router-link to="/">
      user
    </router-link>      
  </li>  
</ul>
<hr>
<router-view></router-view>
</nav>
  


  </div>
</template>

<script>

import  Test  from "./components/Test";
import User from "./components/User";

export default {
 
  components: {
    Test,
    User,
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
</style>
