<template>
    <div class="conteiner">
        <div class="box">
            <h1>{{title}}</h1>
        </div>    
    </div>
</template>
<script>

export default {
    name:'todoList',
    data(){
        return{
            title:'Bem-Vindo a Lista de Tarefas'
        }
    }
   
}
</script>

<style>
    .conteiner{
        background: red;
        width: 300px;
    }
    .box{
        align-items: center;
    }
    body{
        background: rgba(135, 208, 135, 0.712);
    }

</style>