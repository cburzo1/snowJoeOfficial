<template>
  <div>
    <Header/>
    <div class ="main">
      <h2>Quiz 1 - HTML / CSS / JS Practice</h2>
      <Panels :questions="questions"/>
      <Footer/>
    </div>
  </div>
</template>

<script>
  import data from './questions.json';
  import Header from './components/Header.vue';
  import Panels from './components/Panels.vue';
  import Footer from './components/Footer.vue'
  
  export default{
    data(){
      return{
        questions: data
      }
    },
    components: {
      Header,
      Panels,
      Footer
    }
  }
  
</script>

<style>
  html, body{
    margin: 0;
    padding: 0;
    background-color: lightgrey;
  }
  .main{
    margin: auto;
    width: 90%;
    margin-top: 50px;
  }
</style>
