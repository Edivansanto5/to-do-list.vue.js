<template>
    <div conteiner>
        <div class="box">
           
            <input type="text" placeholder="Digite sua Tarefa aqui">
            <button>Enviar</button>
            <h2>Tarefas a Fazer</h2>
            <draggable :list="list1" group="people" @change="log">
                <div v-for="(element,index) in list1" :key="element.name">{{list1.name}}{{index}}</div>
            </draggable>
        </div>
        <div class="box">
            <h2>Tarefas Fazendo</h2>
            <draggable :list="list2" group="people" @change="log">
                <div v-for="(element,index) in list2" :key="element.name">{{list2.name}}{{index}}</div>
            </draggable>

            <rawDisplayer :value="list1" title="List 1" />
            <rawDisplayer :value="list2" title="List 2" />
        </div>


    </div>
    
</template>

<script>
import draggable from 'vuedraggable';

export default {
    name: "todoList",
    data() {
        return {
            list1:[
                {name:'Edivan   Santos', id:0},
                {name:'Elenildo Santos', id:1},
                {name:'Elivanda Santos', id:2},
                {name:'Edilson  Santos', id:3},
                {name:'Edilane  Santos', id:4}
            ],
            list2:[
                {name:'Maria',id:5},
                {name:'Antonio Ediglê de Oliveira', id:6},
                {name:'Luzia Rodrigues dos santos',id:7},
                {name:'Basta Loneia',id:8},
                {name:'Querino',id:9},
                {name:'Antonio',id:10},
               
            ]

        };
    },
    components: { 
        draggable 
    },
    methods: {
    add: function() {
      this.list.push({ name: "Juan" });
    },
    replace: function() {
      this.list = [{ name: "Edgard" }];
    },
    clone: function(el) {
      return {
        name: el.name + " cloned"
      };
    },
    log: function(evt) {
      window.console.log(evt);
    }
  }
}
</script>
<style>

</style>