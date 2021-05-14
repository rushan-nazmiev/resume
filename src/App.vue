<template>
  <div id="app">
    <Sidebar/>
  </div>
</template>

<script>
import Sidebar from './components/Sidebar'
import './assets/css/responsive.css'
export default {
  name: 'App',
  data(){
    return{
      todo:['Test1', 'Test2', 'Test3']
    }
  },
  components: {
    Sidebar
  }
}
</script>

<style>
#app {

}
</style>
