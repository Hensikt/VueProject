<template>
  <div id="app">
    <Header/>
    <Myths v-bind:myths="myths" v-on:del-myth="deleteMyth"/>
  </div>
</template>

<script>
  import Header from "./components/layout/Header";
  import Myths from './components/Myths'

export default {
  name: 'app',
  components: {
    Header,
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
  },
  methods: {
    deleteMyth(id){
      this.myths = this.myths.filter(myth => myth.id !== id);
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
