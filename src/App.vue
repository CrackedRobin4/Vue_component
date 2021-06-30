<template>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.2/css/bulma.min.css">
  <div class="columns">
    <div class="column">
      
    </div>
    <div class="column">
      <div class="box is-primary">
      <input type="text" v-model="data">
      <button @click="addCard">Submit</button>
      <ul>
        <Card v-for="card in cards" :key="card.id" :title="card.title"></Card>
      </ul>
  </div>
    </div>
    <div class="column">
      
    </div>

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
      nextId: 0,
      data: '',
      cards: []
    }
  },
  methods: {
    addCard() {
      this.cards.push({ id: this.nextId++, title: this.data });
      this.data = ''
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
li {
  list-style-type: none;
  border: 2px, double, black;
  padding: 5px;
}
</style>
