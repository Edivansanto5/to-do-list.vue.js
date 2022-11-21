<template>
     <div class="conteiner">
    <h3>Digite um item</h3>
    <input type="text" v-model.trim="lista.text" placeholder="Digite Qualque coisa"> <!-- ok-->
    <button type="button" @click="addLista()" > Enviar</button>

    <div v-for="(lista, index) in listas" :key="index" >
        <span>{{ lista.text }}</span> 
        <button class="btn">A fazer</button>
        <button class="btn">Fazendo</button>
        <button class="btn">Feito</button>
        <button class="btn-excluir" @click="deleta">Excluir</button>
        
    </div>
    <br>
  </div>
   
</template>
<script>

export default {
    name:'todoList',
        data(){
        return{
        lista: {},
        listas: [],
        }
    },
    methods:{
        addLista(){ 
            this.listas.push(this.lista) // add um item na lista
            this.lista = {
                text: '',
            }          
        },
        deleta(){
        this.listas.pop(this.listas)
        console.log('veio parar aqui');                                                            
    
        }, 
    } 
}
</script>

<style>
   .btn{
       background: cornsilk;
   }
   .btn-excluir{
       background: red;
       font-size: large;
       
   }

    
</style>