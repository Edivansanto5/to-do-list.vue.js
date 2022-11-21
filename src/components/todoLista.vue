<template>
    <div conteiner>
        <div class="box">
            <h1>Todo-List</h1>
            <input type="text" placeholder="Digite sua Tarefa aqui">
            <button>Enviar</button>
            <h1>Tarefas a Fazer</h1>
            <draggable>
                <div :list="list1">

                </div>
            </draggable>
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
    }
}
</script>
<style>

</style>