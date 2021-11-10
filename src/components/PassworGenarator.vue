<template>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Arvo:wght@700&display=swap" rel="stylesheet">
<div class="exercise">

<h1>{{title}}</h1>

<form action="" class="form_wrapper">
    
<input type="text" value="copy" id="myCopy"> 
<button class="copy-to-clipboard">Copy to Clipboard 📋 </button>
</form>
<br>
<br>
<p>Choose your Character set:</p>

<div class="button-wrapper">
    <div class="button-row">
        <div class="button-col "><button id="button-lowercase " class="newbutton">Lowercase</button></div>
        <div class="button-col "><button id="button-uppercase newbutton" class="newbutton">Uppercase</button></div>
        <div class="button-col "><button id="button-numbers newbutton" class="newbutton">Numbers</button></div>
        <div class="button-col "><button id="button-symbols newbutton" class="newbutton">Symbols</button></div>
    </div>
</div>
<br>

<h6>Password Length:</h6>

<div class="slider">
    <input type="range" id="password-setting" min="8" max="35">
    <label for="count"></label>
</div>







</div>


  
</template>

<script>
export default {
data(){
    return{
        title:"PASSWORD GENERATOR"
    }
}
}
</script>

<style scoped >

@media  (max-width: 768px) {
    


              .form_wrapper{
                  display: block;
                 margin: 0 auto;
                 
                 
                 
              }
              h1{
                  color: #2292A4;
                  margin-bottom: 70px;}
              
              
              .button-wrapper{
                  
                  justify-content: center;
                  display:flex;
                  
                  
                  flex-grow: 1;
                  flex-shrink: 1;
              }
              
              .button-row{
                  
                  flex-basis: 100%;
                  
              }
              
              div.button-col{
                  display: inline-block;
                  
                  width: 50%;
                  margin-top: 5px;
                  
                  
              }
              
            
            


}

  .newbutton{
                  padding: 0.4em;
                  
                  border-radius: 5px;
                  background-color: #0F0A0A;
                  color: slategrey;
              }
              

  input{
                  color: #F5EFED;
                  text-align: center;
                  width: 80%;
                  height: 30px;
                  background-color:slategrey;
              }
label{
    color: #F5EFED;
}



.copy-to-clipboard{
    display: block;
    background: #2292A4;
    margin: 0 auto;
    padding: 0.6em;
    
    
}
#myCopy{display: block;
margin: 0 auto;
margin-bottom: 20px;}

                   @media  (min-width: 768px){
                       h1{
                       margin-bottom: 50px;
                   }
                   
                   .button-wrapper{
                       
                       justify-content: center;
                       display:flex;
                       
                       flex-grow: 1;
                       flex-shrink: 1;
                       
                   }
                   
                   .button-row{
                       
                       flex-basis: 100%;
                       display: flex;
                       align-content:space-between;
                       justify-content: center;
                       margin-top: 10px;
                       
                       
                   }
                   
                   div.button-col{
                       display: inline-block;
                       
                      
                       margin-top: 5px;
                       margin: 5px;
                       
                   }
                   }
                   
</style>