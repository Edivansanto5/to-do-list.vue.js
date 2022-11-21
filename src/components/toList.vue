<!-- <template>
  <div class="conteiner">
    <h1>Todo-List</h1>
    <input type="text" v-model.trim="lista.text" placeholder="Digite Qualque coisa">
    <button type="button" @click="addLista()" > Enviar</button>

    <div v-for="(lista, index) in listas" :key="index">
    
        <span>{{ lista.text }}</span> 
        <button class="btn" @click="fazer()">A fazer</button>
        <button class="btn" @click="fazendo()">Fazendo</button>
        <button class="btn" @click="feito()">Feito</button>
        <button class="btn-excluir" @click="deleta">Excluir</button>
      
    </div>
    <br>
    <br>
  </div>
    
</template>
<script>

export default {
  name:'toList', 
  data(){
    return{
      lista: {
        checked: false,
        text: '',
        lista2: {
        checked: false,
        text: '',
      },
,
      listas: [],
    }
  },
  methods:{
    addLista(){
      this.listas.push(this.lista) // add um item na lista
      this.lista = {
        checked: false,
        text: '',
      }          
    },
    fazer(){
      // var array = new Array();
      //   $('select option:selected').each(function(index, el) {
      //   array.push($(el).val());
      // });
      // console.log(array);
      console.log('está por fazer');
    },
    fazendo(){
      console.log('está fazendo');
    },
    feito(){
      console.log('está feito');
    },
    // changeChecked (index) {
    //   this.listas[index].checked = !this.listas[index].checked
    //   console.log(this.listas[index].checked) 
    // },
    deleta(){
      
      this.listas.pop(this.listas)
      console.log('veio parar aqui');                                                            
  
    },

  }
 
} -->

<!-- </script>

<style>
  body{
    background: #4fc08c;
    margin: 5px;
  }
  .conteiner{
    background: white;
    max-height: 500px;
    padding-top: 15px;  
    text-align: center; 
    border-radius: 15px;
   
  }
 
  button{
    border-radius: 10px;
    background: #4fc08c;
    width: 120px;
    height: 40px;
    margin: 5px;
    font-size: 20px;

  }
  .btn{
    border-radius: 10px;
    background: #5cb2e4;
    width: 140px;
    height: 40px;
    margin: 5px;
    font-size: 22px;
    opacity: 85%;

  }
  .btn-excluir{
    background: red;
    opacity: 85%;
    
  }

  li{
    padding-top: 10px;
  }
  a{
    color: red;
  }

  .line-through {
    text-decoration: line-through;
    color: rgba(0, 0, 0, 0.3);
  }

  .list {
    display: flex;
    justify-content: justify;
    padding-left: 160px;
    margin-top: 15px;
    margin-bottom: 15px;
    font-size: 28px;
  }

  .mr-10 {
    margin-right: 10px;
  }
  input{
    font-size: 22px;
  }

</style> --> 