<template>
  <header>
    <NavBar/>
  </header>
  
  <div class="main-wrapper">
    <div class="main-container">
      <MainCard/>
      <!-- <ProjectsCard/> -->
    </div>
  </div>

  <footer>
    <FooterCard/>
  </footer>
  
  <!-- <MaintenancePage/> -->
</template>

<script>
  import NavBar from './components/NavBar.vue';
  import MainCard from './components/MainCard.vue'
  import FooterCard from './components/FooterCard.vue';
  // import ProjectsCard from './components/ProjectsCard.vue';
  // import MaintenancePage from './components/MaintenancePage.vue';

  export default {
    name: 'App',
    components: {
      NavBar,
      MainCard,
      FooterCard
      // ProjectsCard,
      // MaintenancePage
    }
  }
</script>

<style>
body{
  height: inherit;
}

  #app {
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }

    .main-wrapper{
      display: flex;
      align-content: center;
      justify-content: center;
      padding-bottom: 200px;
    }

      .main-container{
        width: 70%;
        min-height: 100vh;
      }

@media (max-width: 950px){
  .main-container{
    width: 80%;
  }
        
}
</style>
