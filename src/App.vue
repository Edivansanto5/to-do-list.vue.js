<template>
  <div>
    <toList/> 
    <hr>
    <todoLista/>
  </div>
</template>
<script>

import toList from './components/toList.vue'
import todoLista from './components/todoLista.vue'

  export default{
    components:{
     toList,
     todoLista
  
    }
  }
</script>