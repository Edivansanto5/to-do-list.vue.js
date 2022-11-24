<template>
    <div class="conteiner">
        <div class="box">
            <h1>{{title}}</h1>
        </div> <br> 
        <form class="tarefas">
            <h1>{{nome}}</h1>
            <button class="btn" type="###">Status</button>
            <input type="text" placeholder="Digite aqui uma Tarefa"> 
            <button class="btn" @click="addLista()">Adcionar</button>
           
            
            <br><br>
            <!-- <img src="../assets/excluir.png" @click="apertou()"> -->
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
           
        }
    },
   
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
    .select,.btn{
        padding-left: 10px;
        margin: 12px;
    }
    img{
        width: 40px;
        
    }

    

    
</style>