<template>
  <div class="conteiner">
    <form >
      <h3>Digite um item</h3>
      <input type="text">
        <button type="button" @click="adicionar"> Enviar</button>
        <ul>
          <li v-for="lista in listas" :key="lista">lista1</li>
          
        </ul>
    </form>
  </div>
    
</template>
<script>

export default {
  name:'toList', 
  data(){
    return{
      listas:['lista1','lista2','lista3']
    }
  },
  methods:{
  adicionar(){
    console.log('você clicou !!!!!');
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