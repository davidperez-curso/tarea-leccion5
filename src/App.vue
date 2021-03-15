<template>
  <div id="app" class="container">
    <Header/>
    <Home/>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'
import Home from './components/Home.vue'

export default {
  name: 'App',
  components: {
    //HelloWorld
    Header,
    Home
  }
}
</script>


