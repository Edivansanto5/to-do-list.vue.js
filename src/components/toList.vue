<template>
  <div class="conteiner">
    <form >
      <h3>Digite um item</h3>
      <input type="text" v-model="lista">
        <button type="button" v-on:click="addLista"> Enviar</button>
        <ul>
          <li v-for="lista in listas" :key="lista">{{lista}}</li>
          
        </ul>
    </form>
  </div>
    
</template>
<script>

export default {
  name:'toList', 
  data(){
    return{
      lista:"",
      listas:['lista1','lista2','lista3']
    }
  },
  methods:{
    addLista(){
      this.listas.push(this.lista) // add um item na lista
      this.lista = ""             // remove limpa o canto do imput

    }
    
  }
 
}
</script>

<style>
  body{
    background: #4fc08c;
  }
  .conteiner{
    background: white;
    width: 600px;
    height: 400px;
    padding-top: 15px;  
    text-align: center; 
    border-radius: 15px;
  }
  .teste{
    background: blue;
  }
  button{
    border-radius: 50px;
    background: #4fc08c;
    width: 60px;
    margin: 5px;

  }
</style>