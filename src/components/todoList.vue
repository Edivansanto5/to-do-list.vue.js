<template>
     <div class="conteiner">
    <h3>Digite um item</h3>
    <input type="text" v-model.trim="lista.text" placeholder="Digite Qualque coisa"> <!-- ok-->
    <button type="button" @click="addLista()" > Enviar</button>

    <div v-for="(lista, index) in listas" :key="index" >
        <span>{{ lista.text }}</span> <a class="mr-10" href="#" @click="deleta">Excluir</a>
        <span>{{listas.text}}</span>
    </div>
    <br>
  </div>
    <!-- <div class="conteiner">
      <div class="box">
            <h1>{{title}}</h1>
        </div>
        <h1>{{nome}}</h1>
        <button class="btn" type="###">Status</button>
        <input type="text" v-model="lista.text" placeholder="Digite aqui uma Tarefa"> 
        <button class="btn" @click="addLista()">Adcionar</button>

        <div v-for="(lista,index) in listas" :key="index">
           <p>fasdfadfaf</p>
        </div>
        
   
    </div> -->
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
    

    
</style>