<template>
  <div>
    <toList/> 
    <!-- <todoLista/> -->
  </div>
</template>
<script>

import toList from './components/toList.vue'
// import todoLista from './components/todoLista.vue'
// import '@fortawesome/fontawesome-free/css/all.css'
// import '@fortawesome/fontawesome-free/js/all.js'

  export default{
    components:{
     toList,
    //  todoLista
  
    }
  }
</script>