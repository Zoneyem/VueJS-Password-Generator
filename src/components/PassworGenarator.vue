<template >
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Arvo:wght@700&display=swap" rel="stylesheet">
<div class="exercise">

<h1 >{{title}}</h1>

<h6>{{welc}}</h6>

<form action="" class="form_wrapper" >
    
<input v-on:load="randompass" type=""  id="myCopy" minlength="8"  required v-model="password"> 
<div class="output">

</div>
<button  class="copy-to-clipboard">{{copy}}  </button>

<br>
<br>
<p>{{choose}}</p>


<div class="button-wrapper">
    <div class="button-row" >
        <div class="button-col " ><div ref="name"  @click="turnLowercase" id="button-lowercase " class="newbutton "  >{{lower}}</div></div>
        <div class="button-col "><div  ref="name" @click="turnUpperCase" id="button-uppercase newbutton" class="newbutton" >{{upper}}</div></div>
        <div class="button-col "><div  ref="name" @click="addNumbers" id="button-numbers newbutton" class="newbutton" >{{num}}</div></div>
        <div class="button-col "><div  ref="name" @click="addSymbols" id="button-symbols newbutton" class="newbutton" >{{sym}}</div></div>
    </div>
</div>
</form>



<br>

<h6>{{length}}</h6>

<div class="slider">
    <output  type="range" id="password-setting" ></output>
        <input type="range" @drag="dragSlider" v-model="value" min="8" max="35"  step="1">
    <label >{{value}}</label>
</div>

<div class="terms">
    <input id="lastcheck" type="checkbox" v-model="terms">
    <label >{{check}}</label> : {{terms}}
</div>







</div>


  
</template>

<script>
export default {
    props:['welc' ] ,
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
        check:" checked",
        value:8,
        isClicked:''
       
        
    }
},


methods:{


addLowercase( ){
console.log('hello');

//this.password+=this.password.Math
//console.log(Math.random(1,35));
//this.password+=Math.random(1,35)


const alphabet = "abcdefghijklmnopqrstuvwxyz"
const randomCharacter = alphabet[Math.floor(Math.random(3,5) * alphabet.length)]

this.password+=randomCharacter



},

  turnLowercase  () {
      this.password =this.password.toLowerCase()
   var element = document.getElementById('button-lowercase')
   element.classList.toggle('isClicked') 




//this.isClicked= !this.isClicked

},

addNumbers(){
const rn=Math.floor(Math.random()*10)
this.password+=rn
return this.password.toLowerCase()

//const add =document.getElementById('button-numbers')
//add.classList.toggle('.newclass')

},

turnUpperCase(){
    this.password =this.password.toUpperCase()
    
},
//addSymbols(){
//    const symbols=[]
//    symbols
//this.isClicked= !this.isClicked
//},
randompass(){
    const alphabet = "abcdefghijklmnopqrstuvwxyz"
    let html = document.querySelector('#html')
    console.log(html);
    console.log('hello');
    alert('loading')
   
   
 let randomAlphabet= ''
  
  console.log('hello');
   for(let i=0; i<8; i++ ){
randomAlphabet+= alphabet.charAt(Math.floor(Math.random() * alphabet))
return randomAlphabet
   }
},
   
   

dragSlider(){
    this.value=this.password
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

.isClicked{
background: #2292A4;
color:black ;
}

.click-color{
    display: block;
    background: #2292A4;
    margin: 0 auto;
    padding: 0.6em;
    
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