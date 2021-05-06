<template>
  <div id="app">
     <!-- Header -->
      <Header/>

      <!-- Main -->
      <Jumbotron/>
      <Series/>
      <Services/>
      
      <!-- Footer -->
      <Footer/>  
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import Jumbotron from '@/components/Jumbotron.vue';
import Series from '@/components/Series.vue';
import Services from '@/components/Services.vue';
import Footer from '@/components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,   
    Jumbotron, 
    Series,
    Services,
    Footer,
  }
}
</script>

<style lang="scss">
/* Generals */
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Layout */
.container{
    max-width: 1200px;
    margin: 0 auto;
    font-family: 'Fira Sans Condensed', sans-serif;
}

.flex{
    display: flex;
}  
</style>
