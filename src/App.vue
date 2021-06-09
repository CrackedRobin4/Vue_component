<template>
  <div id="c1">
    <input type="text" id="input">
    <button @click="click">Submit</button>
    <Card :title="title"> </Card>
  </div>
</template>

<script>
import Card from './components/Card.vue'

export default {
  name: 'App',
  components: {
    Card
  },
  data() {
    return {
      title: 'Miras'
    }
  },
  methods: {
    click() {
      this.title = document.getElementById("input").value
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
