<template>
  <div class="conteiner">
    <div>
      <h1>Todo-List</h1>
    <input type="text" placeholder="Digite sua Tarefa">
    <button>Enviar</button>
    </div>
   
    <div class="list1">
      <h3>Lista a Fazer</h3>
      <draggable :list="list1" group="people" @change="log">
        <div class="listas" v-for="(element) in list1" :key="element.name">{{ element.name }}</div> 
      </draggable>
    </div>
    <div class="list2">
      <h3>Lista em Andamento</h3>
      <draggable :list="list2" group="people">
        <div class="listas" v-for="(element) in list2" :key="element.name">{{ element.name }} </div>
      </draggable>
    </div>

    <div class="list3">
      <h3>Lista Concluidas</h3>
      <draggable :list="list3" group="people" @change="log">
        <div class="listas" v-for="(element) in list3" :key="element.name">{{ element.name }}</div>
      </draggable>
    </div>
  </div>
    
</template>
<script>
import draggable from "vuedraggable";

export default {
  // name: "toList",
  // display: "Two Lists",
  // order: 1,
  components: {
    draggable
  },
  data() {
    return {
      list1: [
        { name: "John"},
        { name: "Joao"},
        { name: "Jean"},
        { name: "Gerard"}
      ],
      list2: [
        { name: "Juan"},
        { name: "Edgard"},
        { name: "Johnson"},
        { name: "Talita"}
      ],
      list3: [
        { name: "Edivan"},
        { name: "Edigar" },
        { name: "Jumento"},
        { name: "Cavalona"}
      ]
    };
  },
  // methods: {
  //   add: function() {
  //     this.list.push({ name: "Juan" });
  //   },
  //   replace: function() {
  //     this.list = [{ name: "Edgard" }];
  //   },
  //   clone: function(el) {
  //     return {
  //       name: el.name + " cloned"
  //     };
  //   },
  //   log: function(evt) {
  //     window.console.log(evt);
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
    .conteiner{
      widows: 100%;
      height: 100%;
    }
    .listas{
      margin: 5px;
      padding: 5px;
     
    }
    
  
</style>
