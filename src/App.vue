<template>
  <div id="app">
    <Myths v-bind:myths="myths"/>
  </div>
</template>

<script>
  import Myths from './components/Myths'

export default {
  name: 'app',
  components: {
    Myths
  },
  data(){
    return{
      myths: [
        {
          id: 1,
          title: "Somethin" ,
          completed: false
        },
        {
          id: 2,
          title: "Somewhat",
          completed: true
        },
        {
          id: 3,
          title: "Somehow",
          completed: false
        }
      ]
    }
  }
}
</script>

<style>
  *{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body{
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }
</style>
