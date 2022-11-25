<template>
  <div class="container">
    <div class="box">
      <h1>Todo-List</h1>
      <input type="text" v-model="lista.text" @keyup.enter="addLista(lista.text)" placeholder="Digite Qualquer coisa">
      <button type="button" @click="addLista(lista.text) "> Enviar</button>
    </div>

      <div class="list1">
        <h3>A Fazer</h3>
        <draggable  group="people" >
          
          <div class="listas" v-for="(lista,index) in listas" :key="index"> 
            <span>{{lista.text}}</span>
            
            <a href="#" @click="removeLista(index)" ><i class="fa-solid fa-trash"></i></a>
            
            
          </div>
        </draggable>
      </div>
      
      <div class="list2">
        <h3>Em Andamento</h3>
        <draggable  group="people">
          
        </draggable>
      </div>
      
      <div class="list3">
        <h3>Concluidas</h3>
        <draggable  group="people">
          
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
            // id: 0,
            text: '',
          }
          }  else {
          alert('Por favor, entre com caracteres validos')
        }   
      },
      removeLista : function(index) {
      this.listas.splice(index, 1)
    }
    },
   
  
};
</script>
<style>
  body{
    background: #eee;
    font-size: 20px; 
  
  }

  .list1, .list2, .list3{
    background-color: #fff;
    border-radius: 10px;
    width: 25%;
    display: inline-block;
    margin: 10px;
    box-shadow: 0 .5rem 1.5rem rgba(0, 0, 0, .4);
   }

  h3{
    text-align: center;
  }
  .container{
    widows: 100%;
    height: 100%;
    text-align: center;
    display: flex;
    }
  .listas{
    margin: 5px;
    padding: 5px; 
  }
  input{
    font-size: 22px;
    padding: .3rem;
    margin: 1rem;
    width: 20rem;
    border-radius: 12px;
    background-color: #eee;
  }
  button{
    font-size: 22px;
    padding: .3rem;
    width: 105px;
    border-radius: 10px;
    margin: 10px;
    background:#266DD3;
    color: #fff;
    align-items: center;
    justify-content: center;
    cursor: pointer;
  }
  h1{
    text-align: center;
  }




</style>
