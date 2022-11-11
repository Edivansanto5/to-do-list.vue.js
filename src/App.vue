<template>
  <div>
    <!-- <toList/> -->
    <todoList/>

    
  </div>
</template>
<script>
import todoList from './components/todoList.vue'
// import toList from './components/toList.vue'
import '@fortawesome/fontawesome-free/css/all.css'
import '@fortawesome/fontawesome-free/js/all.js'
  export default{
    components:{
      // toList,
      todoList
    }
  }
</script>