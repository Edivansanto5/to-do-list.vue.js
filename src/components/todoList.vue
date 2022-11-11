<template>
    <div class="conteiner">
        <div class="box">
            <h1>{{title}}</h1>
        </div> <br> 
        <form class="tarefas">
            <h1>{{nome}}</h1>
                <select class="select">
                    <option value="">A fazer</option>
                    <option value="">Fazendo</option>
                    <option value="">Feito</option>
                </select> 
            <input type="text" placeholder="Digite aqui uma Tarefa"> 
            <button>Adcionar</button><img src="../assets/img/close-icon.png" @click="apertou">
            <br><br>
        </form>
    </div>
</template>
<script>

export default {
    name:'todoList',
    data(){
        return{
            title:'TO-DO-LIST',
            nome:'Bem-vindo Ao Gerênciamento de Tarefas',
            status:['A Fazer','Fazendo','Feito'],
            lista:['']
        }
    },methods:{
        apertou(){
            console.log('apertou');
        }
    }  
}
</script>

<style>
    .conteiner {   
        background: white;
        width: 600px;
        height: 80px;
        padding-top: 15px;  
        text-align: center; 
        border-radius: 15px;
   
    }
    .tarefas{
        background: white;
        width: 600px;
        padding-top: 15px;  
        text-align: center; 
        border-radius: 15px;
    }
    body{
        background: #4fc08c;
     
    }
    .select{
        padding-left: 10px;
        margin: 12px;
    }

    

    
</style>