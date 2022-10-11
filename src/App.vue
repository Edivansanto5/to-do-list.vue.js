<template>
  <div id="app">
    <toList/>
  </div>
</template>

<script>
import toList from './components/toList.vue'
export default {
  name: 'App',
  components:{
    toList
  }
}
</script>
<style>
    body{
      background: rgba(0, 183, 255, 0.753) !important;
    }
</style>
