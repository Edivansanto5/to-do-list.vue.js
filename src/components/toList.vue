<template>
    <div class="conteiner">
        <form >
          <h3>Digite um item</h3>
          <input type="text">
          <button type="button" @click="adicionar"> + </button>
        </form>
       
    </div>
</template>
<script>

export default {
  name:'toList', 
  data(){

  },
  methods:{
    adicionar(){
      console.log('clicou');
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
    width: 35px;
    margin: 5px;
  }
</style>