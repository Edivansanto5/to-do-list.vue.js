<template>
  <div class="container">
    <div class="box">
      <h1>Todo-List</h1>
      <input type="text" v-model="lista.text" @keyup.enter="addLista(lista.text)" placeholder="Digite Qualquer coisa">
      <button type="button" @click="addLista(lista.text)" > Enviar</button>

      <draggable :lista="listas" group="people" >
        <div class="listas" v-for="(lista, index) in listas" :key="index"> 
          <span>{{lista.text}}</span>
        </div>
      </draggable>
    </div>

    <div class="list1">
      <h3>Listas a Fazer</h3>
      <draggable :list="list1" group="people" @change="log">
        <div class="listas" v-for="(element) in list1" :key="element.name">{{ element.name }}</div> 
      </draggable>
    </div>
    
    <div class="list2">
      <h3>Listas em Andamento</h3>
      <draggable :list="list2" group="people">
       
      </draggable>
    </div>

    <div class="list3">
      <h3>Listas Concluidas</h3>
      <draggable :list="list3" group="people" @change="log">
       
      </draggable>
    </div>
    
  </div>
  
    
</template>
<script>
import draggable from "vuedraggable";

export default {
 
  data() {
    return {
      lista:{
        text:''
      },
      listas:[],
    
    };
  },
  components: {
    draggable
  },
  methods:{   
      addLista(lista){

        if(lista.trim().length) {

          this.listas.push(this.lista) // add um item na lista
          this.lista = {
            text: '',
          }
          }  else {
          alert('Por favor, entre com caracteres validos')
        }   
      },
    },
    // removeLista(lista) {
    //   if(lista) {
    //   }
    // }

};
</script>
<style>
  body{
    background: #fef6e4;
    font-size: 28px; 
  }
  .list1,.list2,.list3{
    background:#feedc4;
    width: 25%;
    border-radius: 10px;
    display: inline-block;
    margin: 10px;
   }
  h3{
    text-align: center;
  }
  .listas{
    margin: 3px;
    padding: 2px;
  }
  .container{
    widows: 100%;
    height: 100%;
  }
  .listas{
    margin: 5px;
    padding: 5px;   
  }
  input{
    font-size: 22px;
    padding: 5px;
    margin: 15px;
    width: 490px;
    border-radius: 12px;
  }
  button{
    font-size: 22px;
    padding: 5px;
    width: 105px;
    border-radius: 10px;
    margin: 10px;
    background:#f8c44a ;
  }
  h1{
    text-align: center;
  } 
</style>
