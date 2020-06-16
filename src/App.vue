<template>
  <div id="app">
    <keep-alive>
      <component :is="component"></component>
    </keep-alive>
    
    <button @click="component = 'form-one'">Show form one</button>
    <button @click="component = 'form-two'">Show form two</button>
  </div>
</template>

<script>

import formOne from './components/formOne'
import formTwo from './components/formTwo'

export default {
  name: 'App',
  components: {
    'form-one': formOne,
    'form-two': formTwo,
  },
  data () {
    return {
      component: 'form-one'
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
