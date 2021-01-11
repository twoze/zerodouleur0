<template>

 <header>
    <div id="logo"><img src="img/Logo Indolor Dark Render.png" alt="logo"></div>
    <button class="connexion"><a href="user/connexion.php"></a>Se connecter</button>
  </header>
  <main>
    <div id="app">
      <!-- <fieldset> -->
        <div class="check">
        <h1>Notez votre douleur sur 
          une échelle de 1 à 10 :</h1>
        <div class="input"> 
        <input type="radio" id="1" value="1" v-model="douleur">
        <label for="1">1</label>
        <br>
        <input type="radio" id="2" value="2" v-model="douleur">
        <label for="2">2</label>
        <br>
        <input type="radio" id="3" value="3" v-model="douleur">
        <label for="3">3</label>
        <br>
        <input type="radio" id="4" value="4" v-model="douleur">
        <label for="4">4</label>
        <br>
        <input type="radio" id="5" value="5" v-model="douleur">
        <label for="5">5</label>
        <br>
        <input type="radio" id="6" value="6" v-model="douleur">
        <label for="6">6</label>
        <br>
        <input type="radio" id="7" value="7" v-model="douleur">
        <label for="7">7</label>
        <br>
        <input type="radio" id="8" value="8" v-model="douleur">
        <label for="8">8</label>
        <br>
        <input type="radio" id="9" value="9" v-model="douleur">
        <label for="9">9</label>
        <br>
        <input  type="radio" id="10" value="10" v-model="douleur">
        <label for="10">10</label>
      </div>
        <br>
        <button  v-on:click="confirme" class="suite">Suite</button>
        </div>
      <!-- </fieldset> -->
    </div>
  </main>
      
</template>

<script>
       export default{
          name: "checkbox",
          el: "#app",
          data(){
              return {douleur: []
              }
          },
          methods:{
            confirme(){
                  console.warn( this.douleur)
            }
          },
        }
      
</script>

<style>

body{
    background-color: #000C4E;
    color: #ffff;
    font-family: 'Inter', sans-serif;
     margin: 0;
    padding: 0;
    box-sizing: border-box;
}

header{
height: 135px;
display: flex;
justify-content: space-around;
background-color:#243070 ;
align-items: center;
}

main{
    padding: 50px 30px;
}
h1{
    font-size: 16px;
}
#logo{
    text-align: left;
}
.check{
    background-color: #243070;
    border-radius: 26px;
    padding: 20px;
    height: 530px;
}
.input{
    padding-top: 20px;
    display: grid;
}
input[type="radio"]{
    display: none;
}
input[type="radio"] + label {
    position: relative;
    padding-left: 1.3rem;
  }
input[type="radio"] + label::before,
input[type="radio"] + label::after {
  display: block;
  position: absolute;
  box-sizing: border-box;
  bottom: 0;
  left: 0;
  content:'';
  width: 1rem;
  height: 1rem; 
  border-radius: 1rem;
  
}
input[type="radio"]+ label::before {
    background-color: #243070;
    border:#000C4E 2px solid;
}
  input[type="radio"]:checked + label::after {
    background-color: #000C4E;
    border: #243070 2px solid;
}
button{
  position: relative;
  color: #ffff;
  left: 30%;
  width: 130px;
  height: 36px;
  margin: 10px 0 0 28px;
  padding: 7px 29px 9px 23px;
  text-align: center;
  border-radius: 20px;
  border: solid 1px #707070;
  background-color: #00dcc2;
}
.connexion{
    color: black;
    width: 135px;
    margin: 0 ;
    padding: 0;
    position: initial;
}
@media screen 
  and (min-device-width: 1200px) 
  and (max-device-width: 1600px) 
  and (-webkit-min-device-pixel-ratio: 1) { 
      .check{
          width: 20%;
          margin: 0 auto;
      }
}
</style>