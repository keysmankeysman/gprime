<template>
  <div id="app">
    <toolbar></toolbar>
    <router-view></router-view> 
  </div>
</template>

<script>
import Toolbar from './components/Toolbar'

export default {
  data() {
    return {}
  },
  components: {
    Toolbar
  }
}



</script>


<style lang="scss">


</style>
