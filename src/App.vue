<template>
  <div>
    <input type="text" v-model="data">
    <button @click="addCard">Submit</button>
    <ul>
      <Card v-for="card in cards" :key="card.id" :title="card.title"></Card>
    </ul>
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
      newCardText : '',
      data: '',
      cards: []
    }
  },
  methods: {
    addCard() {
      this.newCardText = this.data;
      this.cards.push({ id: this.nextId++, title: this.newCardText });
      this.newCardText = '';
      console.log(this.cards);
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
