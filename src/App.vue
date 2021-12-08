<template>
  
  
  
  <PasswordGenerator welc="Welcome to my first vue App" />
</template>

<script>

import PasswordGenerator from './components/PassworGenarator.vue'

export default {
  name: 'App',
  props:["welc "] ,
  
  components: {
    PasswordGenerator
  },

  data(){
    return{
      
    }
  },
  methods:{
    
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
