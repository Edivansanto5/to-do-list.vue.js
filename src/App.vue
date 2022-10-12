<template>
  <div class="conteiner">
    <form >
      <h3>Digite um item</h3>
      <input type="text" v-model.trim="lista.text" placeholder="Digite Qualque coisa">
        <button type="button" @click="addLista()" > Enviar</button>

        <!-- <ul>
          <li  v-for="lista in listas" :key="lista">
            {{ lista.text }}
            <a href="#" @click="deleta">Excluir</a>
          </li>
        </ul> -->

        <div v-for="(lista, index) in listas" :key="index" class="list">
          <form class="mr-10" >
            <input :id="index" type="checkbox" v-model="lista.checked" @click="changeChecked(index)" />
          </form>

          <span :class="listas[index].checked ? 'line-through mr-10' : 'mr-10'" >{{ lista.text }}</span>

          <a class="mr-10" href="#" @click="deleta">Excluir</a>
          <img src="" alt="">
        </div>
    </form>
    <br>
  </div>
    
</template>
<script>
export default {
  name:'toList', 
  data(){
    return{
      lista: {
        checked: false,
        text: '',
      },
      listas: [],
    }
  },
  methods:{
    addLista(){
      this.listas.push(this.lista) // add um item na lista
      this.lista = {
        checked: false,
        text: '',
      }          // testes commit
    },
    deleta(){
      this.listas.pop(this.lista)
    },
    
    changeChecked (index) {
      this.listas[index].checked = !this.listas[index].checked
      console.log(this.listas[index].checked)
    }
    
  }
 
}
</script>

<style>
  body{
    background: #4fc08c;
    margin: 5px;
  }
  .conteiner{
    background: white;
    max-height: 500px;
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
  ul{
    
    text-align: justify;
  }
  li{
    padding-top: 10px;
  }
  a{
    color: red;
  }
  .line-through {
    text-decoration: line-through;
    color: rgba(0, 0, 0, 0.3);
  }
  .list {
    display: flex;
    justify-content: center;
    margin-top: 15px;
    margin-bottom: 15px;
  }
  .mr-10 {
    margin-right: 10px;
  }
  
</style>