<template>
  
  
  
  <PasswordGenerator />
</template>

<script>

import PasswordGenerator from './components/PassworGenarator.vue'

export default {
  name: 'App',
  props:{
    
  } ,
  
  components: {
    PasswordGenerator
  },

  data(){
    return{
      
    }
  }
}

 





</script>

<style >
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
