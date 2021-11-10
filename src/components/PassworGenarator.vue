<template>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Arvo:wght@700&display=swap" rel="stylesheet">
<div class="exercise">

<h1>{{title}}</h1>

<form action="" class="form_wrapper">
    
<input type=""  id="myCopy" minlength="8" pattern="/[a-z]{8,}/" required v-model="password"> 
<button class="copy-to-clipboard">{{copy}}  </button>
</form>

<br>
<br>
<p>{{choose}}</p>

<div class="button-wrapper">
    <div class="button-row">
        <div class="button-col "><button id="button-lowercase " class="newbutton">{{lower}}</button></div>
        <div class="button-col "><button id="button-uppercase newbutton" class="newbutton">{{upper}}</button></div>
        <div class="button-col "><button id="button-numbers newbutton" class="newbutton">{{num}}</button></div>
        <div class="button-col "><button id="button-symbols newbutton" class="newbutton">{{sym}}</button></div>
    </div>
</div>
<br>

<h6>{{length}}</h6>

<div class="slider">
    <input type="range" id="password-setting" min="8" max="35" value="^/[a-z]{8}/$" step="1" >
    <label ></label>
</div>

<div class="terms">
    <input id="lastcheck" type="checkbox" v-model="terms">
    <label >{{check}}</label> : {{terms}}
</div>







</div>


  
</template>

<script>
export default {
data(){
    return{
        title:"PASSWORD GENERATOR",
        copy:"Copy to Clipboard 📋",
        choose:"Choose your Character set:",
        length:"Password Length",
        password:'',
        upper:"Uppercase",
        lower:"Lowercase",
        num:"Numbers",
        sym:"Symbols",
        terms:"",
        check:" checked"
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

#lastcheck{
    display: block;
}

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