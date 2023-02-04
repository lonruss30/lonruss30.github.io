<template>
  <header>
    <NavBar/>
  </header>
  
  <div class="main-wrapper">
    <div class="main-container">
      <MainCard/>
      <ProjectsCard/>
    </div>
  </div>
  
</template>

<script>

import NavBar from './components/NavBar.vue';
import MainCard from './components/MainCard.vue'
import ProjectsCard from './components/ProjectsCard.vue';


export default {
  name: 'App',
  components: {
    NavBar,
    MainCard,
    ProjectsCard
  }
}
</script>

<style>
body{
  margin: 0;
  padding: 0;
}

.main-wrapper{
  max-width: 100%;
  flex: 1 1 auto;
}

.main-container{
  width: 100%;
  padding-bottom: 100px;
  margin-left: auto;
  margin-right: auto;
}

#app {
  font-family: 'Poppins', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #395144;
  background-color: #F0EBCE;
}
</style>
